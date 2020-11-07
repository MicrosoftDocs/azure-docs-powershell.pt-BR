---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777102"
---
# <span data-ttu-id="f1c42-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="f1c42-101">Get-AzsOffer</span></span>

## <span data-ttu-id="f1c42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1c42-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c42-103">Obtenha a lista de ofertas públicas para o provedor raiz.</span><span class="sxs-lookup"><span data-stu-id="f1c42-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="f1c42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1c42-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f1c42-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1c42-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c42-106">Obtenha a lista de ofertas públicas para o provedor raiz.</span><span class="sxs-lookup"><span data-stu-id="f1c42-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="f1c42-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1c42-107">EXAMPLES</span></span>

### <span data-ttu-id="f1c42-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1c42-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="f1c42-109">Obter a lista de ofertas públicas</span><span class="sxs-lookup"><span data-stu-id="f1c42-109">Get the list of public offers</span></span>

## <span data-ttu-id="f1c42-110">OS</span><span class="sxs-lookup"><span data-stu-id="f1c42-110">PARAMETERS</span></span>

### <span data-ttu-id="f1c42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c42-111">-DefaultProfile</span></span>
<span data-ttu-id="f1c42-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c42-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1c42-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c42-113">CommonParameters</span></span>
<span data-ttu-id="f1c42-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c42-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c42-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1c42-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c42-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1c42-116">INPUTS</span></span>

## <span data-ttu-id="f1c42-117">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1c42-117">OUTPUTS</span></span>

### <span data-ttu-id="f1c42-118">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="f1c42-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="f1c42-119">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1c42-119">NOTES</span></span>

## <span data-ttu-id="f1c42-120">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1c42-120">RELATED LINKS</span></span>

