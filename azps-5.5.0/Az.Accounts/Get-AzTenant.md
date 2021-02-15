---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114336"
---
# <span data-ttu-id="ee229-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="ee229-101">Get-AzTenant</span></span>

## <span data-ttu-id="ee229-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee229-102">SYNOPSIS</span></span>
<span data-ttu-id="ee229-103">Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ee229-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="ee229-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee229-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee229-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee229-105">DESCRIPTION</span></span>
<span data-ttu-id="ee229-106">O Get-AzTenant cmdlet obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ee229-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="ee229-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee229-107">EXAMPLES</span></span>

### <span data-ttu-id="ee229-108">Exemplo 1: Obter todos os locatários</span><span class="sxs-lookup"><span data-stu-id="ee229-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="ee229-109">Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee229-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="ee229-110">Exemplo 2: Obter um locatário específico</span><span class="sxs-lookup"><span data-stu-id="ee229-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="ee229-111">Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee229-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="ee229-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee229-112">PARAMETERS</span></span>

### <span data-ttu-id="ee229-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee229-113">-DefaultProfile</span></span>
<span data-ttu-id="ee229-114">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ee229-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee229-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ee229-115">-TenantId</span></span>
<span data-ttu-id="ee229-116">Especifica a ID do locatário que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ee229-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ee229-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee229-117">CommonParameters</span></span>
<span data-ttu-id="ee229-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee229-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee229-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee229-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee229-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="ee229-120">INPUTS</span></span>

### <span data-ttu-id="ee229-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ee229-121">System.String</span></span>

## <span data-ttu-id="ee229-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="ee229-122">OUTPUTS</span></span>

### <span data-ttu-id="ee229-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ee229-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="ee229-124">Notas</span><span class="sxs-lookup"><span data-stu-id="ee229-124">NOTES</span></span>

## <span data-ttu-id="ee229-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee229-125">RELATED LINKS</span></span>
