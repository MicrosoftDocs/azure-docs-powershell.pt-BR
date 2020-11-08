---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116488"
---
# <span data-ttu-id="0dfe4-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="0dfe4-101">Get-AzTenant</span></span>

## <span data-ttu-id="0dfe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dfe4-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfe4-103">Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0dfe4-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="0dfe4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dfe4-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dfe4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dfe4-105">DESCRIPTION</span></span>
<span data-ttu-id="0dfe4-106">O cmdlet Get-AzTenant Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0dfe4-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="0dfe4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dfe4-107">EXAMPLES</span></span>

### <span data-ttu-id="0dfe4-108">Exemplo 1: obtendo todos os locatários</span><span class="sxs-lookup"><span data-stu-id="0dfe4-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="0dfe4-109">Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dfe4-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="0dfe4-110">Exemplo 2: obtendo um locatário específico</span><span class="sxs-lookup"><span data-stu-id="0dfe4-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="0dfe4-111">Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dfe4-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="0dfe4-112">OS</span><span class="sxs-lookup"><span data-stu-id="0dfe4-112">PARAMETERS</span></span>

### <span data-ttu-id="0dfe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfe4-113">-DefaultProfile</span></span>
<span data-ttu-id="0dfe4-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0dfe4-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dfe4-115">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="0dfe4-115">-TenantId</span></span>
<span data-ttu-id="0dfe4-116">Especifica a ID do locatário que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0dfe4-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0dfe4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfe4-117">CommonParameters</span></span>
<span data-ttu-id="0dfe4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dfe4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfe4-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dfe4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfe4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dfe4-120">INPUTS</span></span>

### <span data-ttu-id="0dfe4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0dfe4-121">System.String</span></span>

## <span data-ttu-id="0dfe4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dfe4-122">OUTPUTS</span></span>

### <span data-ttu-id="0dfe4-123">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="0dfe4-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="0dfe4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dfe4-124">NOTES</span></span>

## <span data-ttu-id="0dfe4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dfe4-125">RELATED LINKS</span></span>
