<script>
    import FaqComp from '../component/faq-comp.svelte';

    let array = [
	            {
                    title: "Most Common Questions",
                    questionList: [
                        {
                            question: "Which location does the platform cover?",
                            answer: "Zoneomics provides national coverage on demand and is expanding coverage weekly. We can add any city within 7 days."
                        },
                        {
                            question: "Which location does the platform cover?",
                            answer: "More zoning data enables you to make better faster appraisal decisions. Stop visiting multiple city websites to find zoning maps. Easily access up-to-date permitted land uses, lot size, FAR, and building height of the property, all in one place.Understand the specific zoning of a property in any city in the U.S. Stop waiting in line at city zoning departments and battling through 2,000 pages of zone codes, and do your own zoning analysis with Zoneomic's platform!"
                        },
                        {
                            question: "How simple is it to use zoneomics?",
                            answer: "Zoneomics is designed to be very user-friendly. Most users get up and running on their own and like to make use of our tutorials and documentation. Our Client Success team is responsive to answer questions and help you make the most out of Zoneomics."
                        }
		                        ]
	            },


                {
                    title: "Billing Questions",
                    questionList: [
                        {
                            question: "Can I customize my payments?",
                            answer: "Most users pay annually to save money. Some people prefer the flexibility of paying monthly or using pay-as-you-go credits. If you require a customized package specific to your needs, reach out to our team, and we can search for options to help you maximize your potential using Zoneomics."
                        },
                        {
                            question: "What is your cancellation policy?",
                            answer: "Payment obligations for use of the Zoneomics Services are non-cancelable and Fees paid are non-refundable."
                        }
                    ]
                }

]
</script>


<FaqComp {array} />
    