<template>
  <div class="store-wrapper">
    <div class="store-container">
      <h2 class="wishlist-title secondary-font mb-3">STORE LOCATOR</h2>
      <div class="content-pages">
        <div class="location-div">
          <label></label>
          <div class="store-search_box">
            <p>Find stores near this location</p>
            <div class="input-box">
              <input
                type="text"
                placeholder="Start searching here"
                autocomplete="off"
                v-model="search"
              />
            </div>
          </div>
        </div>

        <div class="col-1">
          <div class="store-left">
            <ul class="sidebar-store">
              <!-- <li
                v-for="store in filteredStores"
                class="store-locator-result"
                :key="store"
              > -->
                <h4>
                  <!-- <svg-wrapper
                    class="inline-svg mr-2"
                    :svg_src="'location'"
                  ></svg-wrapper>
                  <a @click="selectLocation(store)">
                    {{ storeName }}
                  </a> -->
                </h4>
                <!-- <p>
                  {{ store?.name }}, {{ store?.address }}, {{ store?.city }} ,{{
                    store?.state
                  }},{{ store?.pincode }}
                </p> -->
                <!-- <p class="pt-2">
                  <svg-wrapper
                    class="inline-svg mt-2"
                    :svg_src="'telephone'"
                  ></svg-wrapper>
                  +{{ store?.contacts[0]?.country_code }} &nbsp;
                  {{ store?.contacts[0]?.number }}
                </p> -->
              <!-- </li> -->
            </ul>
          </div>
        </div>

        <!-- <div class="col-2">
          <Google-map
            :markers="markers"
            ref="map"
            :mapConfig="mapConfig"
            :apiKey="googleMapsApiKey"
          ></Google-map>
        </div> -->
      </div>
    </div>
    <!-- <fdk-loader v-if="inProgress"></fdk-loader> -->
  </div>
</template>

<script>
// import root from "window-or-global";
// import { isBrowser } from "browser-or-node";
// import debounce from "lodash/debounce";
// import googleMapLoader from "../global/components/google/GoogleMapLoader.vue";
// import {
//   GOOGLE_MAPS_API_KEY,
//   mapSettings,
// } from "../global/components/google/mapSettings";
// import SvgWrapper from "../components/common/svg-wrapper.vue";

export default {
  name: "storelocator",
  components: {
    // "Google-map": googleMapLoader,
    // "svg-wrapper": SvgWrapper,
  },
  // mounted() {
  //   root.FPI?.state?.theme?.globalConfig?.subscribe((res) => {
  //     this.googleMapsApiKey =
  //       res.props?.googleMapsApiKey || GOOGLE_MAPS_API_KEY;
  //   });
  //   this.isMounted = true;
  //   if (isBrowser) {
  //     if (window.screen.width < 767) {
  //       this.isMobile = true;
  //     }
  //   }
  //   this.getStoresdata();
  //   this.getStoresPaginator();
  // },
  // data() {
  //   return {
  //     markers: [],
  //     popup: false,
  //     filteredStores: [],
  //     googleMapsApiKey: "",
  //     chooseCity: "",
  //     search: "",
  //     storeName: "",
  //     latLngObj: { lat: 19.0653252, lng: 72.8423802 },
  //     isMounted: false,
  //     cityList: [],
  //     stores: [],
  //     pageInfo: [],
  //     page: { current: 0, has_next: true },
  //     selectStore: {},
  //     timing: [],
  //     inProgress: false,
  //   };
  // },
  // watch: {
  //   search: {
  //     handler() {
  //       this.filterStores();
  //     },
  //     immediate: true,
  //   },
  //   stores: {
  //     handler() {
  //       this.cityList = this.filtercities(this.stores);
  //       this.filterStores();
  //     },
  //     immediate: true,
  //   },
  // },

  // computed: {
  //   mapConfig() {
  //     return {
  //       ...mapSettings,
  //       zoom: 4,
  //       center: this.latLngObj,
  //       zoomControlOptions: {
  //         ...mapSettings.zoomControlOptions,
  //       },
  //       fullscreenControl: true,
  //     };
  //   },
  //   storeCount() {
  //     return this.filteredStores?.length;
  //   },
  // },

  // methods: {
  //   convertTime(time) {
  //     if (time < 12) return time + " " + "am";
  //     else return time - 12 + " " + "pm";
  //   },
  //   getDirection(store) {
  //     return `https://maps.google.com/maps?daddr=${store.name},${store.address},${store.pincode}`;
  //   },
  //   filterStores(city = null) {
  //     let filteredArray = [];
  //     let filteredMarkers = [];
  //     this.stores.forEach((element) => {
  //       let searchText =
  //         element.name +
  //         " " +
  //         element.address +
  //         " " +
  //         element.city +
  //         " " +
  //         element.email;
  //       if (searchText.toLowerCase().includes(this.search.toLowerCase())) {
  //         filteredArray.push(element);
  //         filteredMarkers.push({
  //           lat: element.lat_long.coordinates[1],
  //           lng: element.lat_long.coordinates[0],
  //         });
  //       }
  //     });
  //     this.filteredStores = filteredArray;
  //     this.markers = filteredMarkers;
  //   },
  //   selectLocation(store) {
  //     this.inProgress = true;
  //     this.popup = true;
  //     this.selectStore = store;
  //     this.$apiSDK.catalog
  //       .getLocationDetailsById({ locationId: store?.uid })
  //       .then((result) => {
  //         this.timing = result.timing;
  //         this.inProgress = false;
  //       })
  //       .catch((e) => {
  //         this.inProgress = false;

  //         console.log(e);
  //       });

  //     this.latLngObj = {
  //       lat: store.lat_long.coordinates[1],
  //       lng: store.lat_long.coordinates[0],
  //     };
  //     this.$refs.map.setMarkerPosition(this.latLngObj);
  //     this.$refs.map.setInfoWindow(store);
  //   },
  //   getStoresdata() {
  //     this.$apiSDK.configuration.getApplication().then((result) => {
  //       this.storeName = result.name;
  //     });
  //   },
  //   filtercities(arr) {
  //     return [...new Set(arr.map((item) => item.city))];
  //   },
  //   getStoresPaginator(type) {
  //     this.makeCall = false;
  //     this.isLoading = true;
  //     this.page.current = this.page.current + 1;
  //     let options = {
  //       pageNo: this.page.current,
  //       pageSize: 1000,
  //       ...(this.chooseCity && { city: this.chooseCity }),
  //       ...(this.search && { q: this.search }),
  //     };
  //     this.$apiSDK.catalog
  //       .getStores(options)
  //       .then((res) => {
  //         type == "loadMore" ? "" : (this.stores = []);
  //         let item = [...this.stores, ...res.items];
  //         this.stores = item;
  //         this.pageInfo = res.page;
  //         this.noItem = !this.stores.length;
  //         this.hasNext = res.page.has_next;
  //         this.isLoading = false;
  //         this.makeCall = true;
  //         if (
  //           (this.search != "" || this.chooseCity != "") &&
  //           this.page.current == 1
  //         ) {
  //         }
  //       })
  //       .catch((ex) => {
  //         this.isLoading = false;
  //       });
  //   },
  // },
};
</script>
<style lang="less" scoped>
.store-wrapper {
  padding-bottom: 40px;
  padding-top: 24px;
}
.sidebar-store {
  position: relative;
  padding: 0 !important;
  max-height: 450px;
  overflow: auto;
  &::-webkit-scrollbar {
    width: 4px;
  }

  // &::-webkit-scrollbar-track {
  //   -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  //   box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  //   border-radius: 10px;
  // }

  // &::-webkit-scrollbar-thumb {
  //   border-radius: 10px;
  //   -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.5);
  //   box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  // }
  .get-direction {
    a {
      text-decoration: underline;
      text-transform: capitalize;
    }
  }
  .store-locator-result {
    list-style: none;
    border: none;
    cursor: pointer;
    border-top: 1px solid @border-color;
    position: relative;
    text-transform: capitalize;
    padding: 15px 5px 15px 5px;
    min-height: 30px;

    // @media @tablet {
    //   padding: 15px 20px;
    // }
    h4 {
      .inline-svg {
        justify-content: unset !important;
        display: unset !important;
        width: 18px;
        height: 22.5px;
        cursor: pointer;
      }
      a {
        top: -5px;
        position: relative;
        cursor: pointer;
        font-style: normal;
        font-weight: 600;
        font-size: 18px;
        line-height: 130%;
      }
    }
    p {
      margin-left: 25px;
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 130%;
      .inline-svg {
        justify-content: unset !important;
        display: unset !important;
        width: 13px;
        height: 13px;
        cursor: pointer;
      }
    }
  }
}
.store-container {
  max-width: 1180px !important;
  min-height: 100vh;
  margin: 0 auto;
  // @media @tablet-screen {
  //   padding: 50px 40px;
  // }

  // @media @tablet {
  //   box-sizing: border-box;
  //   padding: 50px 0px 0px 0px;
  // }

  .wishlist-title {
    text-align: center;
    font-style: normal;
    font-weight: 600;
    font-size: 28px;
    line-height: 130%;
    &.mb-3 {
      margin-bottom: 1rem !important;
    }
    // @media @tablet {
    //   font-size: 25px;
    //   text-align: center;
    // }
  }
  .content-pages {
    display: flex;
    flex-wrap: wrap;
    box-sizing: border-box;
    margin: 0 auto;

    .location-div {
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;

      position: relative;

      // @media @tablet {
      //   padding: 15px;
      // }

      input {
        padding: 12px 10px;
        font-size: 14px;
        outline: none !important;
        border: 1px solid @border-color;
        border-radius: 0;
        width: 400px;

        &::placeholder {
          margin: 0;
          color: @color-gray;
          padding: 12px;
          font-style: normal;
          font-weight: 400;
          font-size: 14px;
          line-height: 130%;
        }
        // @media @mobile {
        //   width: 90%;
        // }
        // @media @tablet {
        //   width: 90%;
        // }
      }
      .search-icon {
        position: absolute;
        right: 25px;
        cursor: pointer;
        filter: invert(1);
        top: 50%;
        transform: translateY(-50%);
        font-size: 20px;
      }
    }

    .col {
      &-1 {
        flex: 0 0 31.333333%;
        max-width: 31.333333%;
        padding-right: 15px;

        // @media @tablet {
        //   flex: 0 0 100%;
        //   max-width: 100%;
        //   padding-bottom: 50px;
        //   overflow-y: auto;
        //   padding-right: 0;
        // }
        .store-left {
          height: 100%;
          overflow-y: auto;
          position: relative;
          overflow: hidden;
          label {
            font-size: 20px;
            text-transform: uppercase;

            color: @color-black;
            text-decoration: underline;
            display: inline-block;
            margin-bottom: 0.5rem;
          }
          select.city-select {
            text-transform: capitalize;
            font-size: 20px;

            padding-left: 10px;
            background-color: @color-white;
            border: none;
            height: 42px;
            margin-bottom: 18px;
            color: #495057;
            width: 100%;
          }
        }
      }
      &-2 {
        flex: 0 0 66.666667%;
        max-width: 66.666667%;
        @media @tablet {
          flex: 0 0 100%;
          max-width: 100%;
          margin-top: 25px;
        }
        label {
          font-size: 20px;
          text-transform: uppercase;

          color: @color-black;
          text-decoration: underline;
          display: inline-block;
          margin-bottom: 0.5rem;
        }
      }
    }
  }
  .store-search_box {
    margin: 20px 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: @color-gray-1;
    padding: 10px;
    p {
      margin: 0;
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 130%;
    }
    input {
      padding: 12px 10px;
      font-size: 14px;
      outline: none !important;
      border: 1px solid @border-color;
      border-radius: 0;
      width: 400px;
    }
  }
  @media screen and (max-width: 767px) {
    .store-search_box {
      display: flex;
      margin: 20px 0;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      background: @color-gray-1;
      padding: 10px;
      align-items: unset;
    }
    p {
      margin: 0;
      font-size: 14px;
      padding: 10px;
    }
  }
}
</style>
