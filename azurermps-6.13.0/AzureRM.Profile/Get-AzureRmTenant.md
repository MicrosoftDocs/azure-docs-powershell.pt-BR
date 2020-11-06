---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 1d5312cfaf7afb96149ae00b0e7900905206fb3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430093"
---
# <span data-ttu-id="bc427-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="bc427-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="bc427-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc427-102">SYNOPSIS</span></span>
<span data-ttu-id="bc427-103">Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="bc427-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc427-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc427-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc427-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc427-105">DESCRIPTION</span></span>
<span data-ttu-id="bc427-106">O cmdlet Get-AzureRmTenant Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="bc427-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="bc427-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc427-107">EXAMPLES</span></span>

### <span data-ttu-id="bc427-108">Exemplo 1: obtendo todos os locatários</span><span class="sxs-lookup"><span data-stu-id="bc427-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="bc427-109">Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc427-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="bc427-110">Exemplo 2: obtendo um locatário específico</span><span class="sxs-lookup"><span data-stu-id="bc427-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="bc427-111">Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc427-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="bc427-112">OS</span><span class="sxs-lookup"><span data-stu-id="bc427-112">PARAMETERS</span></span>

### <span data-ttu-id="bc427-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc427-113">-DefaultProfile</span></span>
<span data-ttu-id="bc427-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bc427-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc427-115">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="bc427-115">-TenantId</span></span>
<span data-ttu-id="bc427-116">Especifica a ID do locatário que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bc427-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc427-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc427-117">CommonParameters</span></span>
<span data-ttu-id="bc427-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc427-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc427-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc427-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc427-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc427-120">INPUTS</span></span>

### <span data-ttu-id="bc427-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bc427-121">System.String</span></span>

## <span data-ttu-id="bc427-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc427-122">OUTPUTS</span></span>

### <span data-ttu-id="bc427-123">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="bc427-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="bc427-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc427-124">NOTES</span></span>

## <span data-ttu-id="bc427-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc427-125">RELATED LINKS</span></span>
