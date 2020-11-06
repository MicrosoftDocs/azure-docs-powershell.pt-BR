---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 7d9687877e3a27d175719a7a7b9ec6c78a529e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432438"
---
# <span data-ttu-id="405c0-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="405c0-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="405c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="405c0-102">SYNOPSIS</span></span>
<span data-ttu-id="405c0-103">Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="405c0-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="405c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="405c0-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="405c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="405c0-105">DESCRIPTION</span></span>
<span data-ttu-id="405c0-106">O cmdlet Get-AzureRmTenant Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="405c0-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="405c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="405c0-107">EXAMPLES</span></span>

### <span data-ttu-id="405c0-108">Exemplo 1: obtendo todos os locatários</span><span class="sxs-lookup"><span data-stu-id="405c0-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="405c0-109">Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="405c0-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="405c0-110">Exemplo 2: obtendo um locatário específico</span><span class="sxs-lookup"><span data-stu-id="405c0-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="405c0-111">Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="405c0-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="405c0-112">OS</span><span class="sxs-lookup"><span data-stu-id="405c0-112">PARAMETERS</span></span>

### <span data-ttu-id="405c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405c0-113">-DefaultProfile</span></span>
<span data-ttu-id="405c0-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="405c0-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="405c0-115">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="405c0-115">-TenantId</span></span>
<span data-ttu-id="405c0-116">Especifica a ID do locatário que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="405c0-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405c0-117">CommonParameters</span></span>
<span data-ttu-id="405c0-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="405c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405c0-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="405c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405c0-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="405c0-120">INPUTS</span></span>

### <span data-ttu-id="405c0-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="405c0-121">None</span></span>
<span data-ttu-id="405c0-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="405c0-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="405c0-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="405c0-123">OUTPUTS</span></span>

### <span data-ttu-id="405c0-124">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="405c0-124">PSAzureTenant</span></span>
<span data-ttu-id="405c0-125">Esse cmdlet retorna a ID do locatário e as informações de domínio associadas para locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="405c0-125">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="405c0-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="405c0-126">NOTES</span></span>

## <span data-ttu-id="405c0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="405c0-127">RELATED LINKS</span></span>

