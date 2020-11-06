---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425840"
---
# <span data-ttu-id="88a6b-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="88a6b-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="88a6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="88a6b-103">Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="88a6b-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="88a6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88a6b-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="88a6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="88a6b-106">O cmdlet Get-AzureRmTenant Obtém locatários autorizados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="88a6b-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="88a6b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="88a6b-108">Exemplo 1: obtendo todos os locatários</span><span class="sxs-lookup"><span data-stu-id="88a6b-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="88a6b-109">Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="88a6b-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="88a6b-110">Exemplo 2: obtendo um locatário específico</span><span class="sxs-lookup"><span data-stu-id="88a6b-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="88a6b-111">Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="88a6b-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="88a6b-112">OS</span><span class="sxs-lookup"><span data-stu-id="88a6b-112">PARAMETERS</span></span>

### <span data-ttu-id="88a6b-113">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="88a6b-113">-TenantId</span></span>
<span data-ttu-id="88a6b-114">Especifica a ID do locatário que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="88a6b-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="88a6b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a6b-115">CommonParameters</span></span>
<span data-ttu-id="88a6b-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a6b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a6b-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a6b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a6b-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88a6b-118">INPUTS</span></span>

## <span data-ttu-id="88a6b-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88a6b-119">OUTPUTS</span></span>

### <span data-ttu-id="88a6b-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="88a6b-120">PSAzureTenant</span></span>
<span data-ttu-id="88a6b-121">Esse cmdlet retorna a ID do locatário e as informações de domínio associadas para locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="88a6b-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="88a6b-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88a6b-122">NOTES</span></span>

## <span data-ttu-id="88a6b-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88a6b-123">RELATED LINKS</span></span>

