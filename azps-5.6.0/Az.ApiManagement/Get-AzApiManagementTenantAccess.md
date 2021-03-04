---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c19888bd45ae943b60b90172913a83f42a1fd6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892268"
---
# <span data-ttu-id="a4b99-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="a4b99-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="a4b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b99-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b99-103">Obtém a configuração de acesso para um locatário.</span><span class="sxs-lookup"><span data-stu-id="a4b99-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="a4b99-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a4b99-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b99-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a4b99-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b99-106">O cmdlet **Get-AzApiManagementTenantAccess** obtém a configuração de acesso de locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="a4b99-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="a4b99-107">As chaves não serão incluídas nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="a4b99-107">Keys will not be included into result details.</span></span> <span data-ttu-id="a4b99-108">Para obter o segredo do cliente, use **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="a4b99-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="a4b99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4b99-109">EXAMPLES</span></span>

### <span data-ttu-id="a4b99-110">Exemplo 1: Obter configuração de acesso de locatário</span><span class="sxs-lookup"><span data-stu-id="a4b99-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="a4b99-111">Este comando obtém a configuração de acesso do locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="a4b99-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="a4b99-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a4b99-112">PARAMETERS</span></span>

### <span data-ttu-id="a4b99-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a4b99-113">-Context</span></span>
<span data-ttu-id="a4b99-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a4b99-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b99-115">-DefaultProfile</span></span>
<span data-ttu-id="a4b99-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a4b99-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b99-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b99-117">CommonParameters</span></span>
<span data-ttu-id="a4b99-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b99-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b99-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b99-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b99-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4b99-120">INPUTS</span></span>

### <span data-ttu-id="a4b99-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a4b99-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="a4b99-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a4b99-122">OUTPUTS</span></span>

### <span data-ttu-id="a4b99-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="a4b99-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a4b99-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="a4b99-124">NOTES</span></span>

## <span data-ttu-id="a4b99-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4b99-125">RELATED LINKS</span></span>

[<span data-ttu-id="a4b99-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="a4b99-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


