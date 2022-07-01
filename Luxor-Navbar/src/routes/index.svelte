<script>
    import Navbar from '../components/NavbarLuxor.svelte';

    let ListItems1= [

        {
            href:'#',
            title: 'Home'
        },

        
        {
            href:'#',
            title: 'About'
        }
    ]

    let ListItems2= [

        {
            href:'#',
            src:'src/Luxor-Logo.png',
            alt:'Luxor logo'
        }

    ]


    let ListItems3= [
   
        {
            href:'#',
            title: 'Contact'
        },

        
        {
            href:'#',
            title: 'Gallery'
        }

    ];

</script>

<Navbar List_Items1={ListItems1}
        List_Items2={ListItems2} 
        List_Items3={ListItems3}/>