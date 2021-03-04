---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885765"
---
# <span data-ttu-id="b29f6-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="b29f6-101">Get-AzTenant</span></span>

## <span data-ttu-id="b29f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b29f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b29f6-103">Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b29f6-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="b29f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b29f6-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b29f6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b29f6-105">DESCRIPTION</span></span>
<span data-ttu-id="b29f6-106">O Get-AzTenant cmdlet obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b29f6-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="b29f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b29f6-107">EXAMPLES</span></span>

### <span data-ttu-id="b29f6-108">Exemplo 1: Obter todos os locatários</span><span class="sxs-lookup"><span data-stu-id="b29f6-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="b29f6-109">Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="b29f6-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="b29f6-110">Exemplo 2: Obter um locatário específico</span><span class="sxs-lookup"><span data-stu-id="b29f6-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="b29f6-111">Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="b29f6-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="b29f6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b29f6-112">PARAMETERS</span></span>

### <span data-ttu-id="b29f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29f6-113">-DefaultProfile</span></span>
<span data-ttu-id="b29f6-114">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b29f6-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29f6-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b29f6-115">-TenantId</span></span>
<span data-ttu-id="b29f6-116">Especifica a ID do locatário que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b29f6-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b29f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29f6-117">CommonParameters</span></span>
<span data-ttu-id="b29f6-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29f6-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b29f6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29f6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b29f6-120">INPUTS</span></span>

### <span data-ttu-id="b29f6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b29f6-121">System.String</span></span>

## <span data-ttu-id="b29f6-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b29f6-122">OUTPUTS</span></span>

### <span data-ttu-id="b29f6-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="b29f6-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="b29f6-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="b29f6-124">NOTES</span></span>

## <span data-ttu-id="b29f6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b29f6-125">RELATED LINKS</span></span>
