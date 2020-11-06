---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425843"
---
# <span data-ttu-id="4d2ac-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4d2ac-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="4d2ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4d2ac-103">Obtém os metadados usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="4d2ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d2ac-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="4d2ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4d2ac-106">O cmdlet Get-AzureRmContext Obtém os metadados atuais usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="4d2ac-107">Esse cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente de destino do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="4d2ac-108">Os cmdlets do Azure Resource Manager usam essas configurações por padrão ao realizar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="4d2ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d2ac-109">EXAMPLES</span></span>

### <span data-ttu-id="4d2ac-110">Exemplo 1: obtendo o contexto atual</span><span class="sxs-lookup"><span data-stu-id="4d2ac-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="4d2ac-111">Neste exemplo, estamos nos conectando à nossa conta com uma assinatura do Azure usando Add-AzureRmAccount e, em seguida, estamos obtendo o contexto da sessão atual chamando Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="4d2ac-112">OS</span><span class="sxs-lookup"><span data-stu-id="4d2ac-112">PARAMETERS</span></span>

### <span data-ttu-id="4d2ac-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d2ac-113">CommonParameters</span></span>
<span data-ttu-id="4d2ac-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d2ac-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d2ac-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d2ac-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d2ac-116">INPUTS</span></span>

## <span data-ttu-id="4d2ac-117">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d2ac-117">OUTPUTS</span></span>

### <span data-ttu-id="4d2ac-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="4d2ac-118">PSAzureContext</span></span>
<span data-ttu-id="4d2ac-119">Esse cmdlet retorna a conta, o locatário e a assinatura usadas pelos cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4d2ac-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="4d2ac-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d2ac-120">NOTES</span></span>

## <span data-ttu-id="4d2ac-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d2ac-121">RELATED LINKS</span></span>

[<span data-ttu-id="4d2ac-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="4d2ac-122">Set-AzureRMContext</span></span>]()

