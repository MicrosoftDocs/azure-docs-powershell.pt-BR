---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: 56246de86606aeb07dd8ccdbcfbf2dc35b32a5a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892264"
---
# <span data-ttu-id="292f0-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="292f0-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="292f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="292f0-102">SYNOPSIS</span></span>
<span data-ttu-id="292f0-103">Obtém as chaves de configuração de acesso para um locatário.</span><span class="sxs-lookup"><span data-stu-id="292f0-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="292f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="292f0-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="292f0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="292f0-105">DESCRIPTION</span></span>
<span data-ttu-id="292f0-106">Obtém as chaves de configuração de acesso para um locatário.</span><span class="sxs-lookup"><span data-stu-id="292f0-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="292f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="292f0-107">EXAMPLES</span></span>

### <span data-ttu-id="292f0-108">Exemplo 1: Obter chaves de configuração de acesso para locatários</span><span class="sxs-lookup"><span data-stu-id="292f0-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="292f0-109">Este comando obtém as chaves de configuração de acesso do locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="292f0-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="292f0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="292f0-110">PARAMETERS</span></span>

### <span data-ttu-id="292f0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="292f0-111">-Context</span></span>
<span data-ttu-id="292f0-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="292f0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="292f0-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="292f0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="292f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292f0-114">-DefaultProfile</span></span>
<span data-ttu-id="292f0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="292f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="292f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292f0-116">CommonParameters</span></span>
<span data-ttu-id="292f0-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292f0-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="292f0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292f0-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="292f0-119">INPUTS</span></span>

### <span data-ttu-id="292f0-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="292f0-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="292f0-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="292f0-121">OUTPUTS</span></span>

### <span data-ttu-id="292f0-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="292f0-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="292f0-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="292f0-123">NOTES</span></span>

## <span data-ttu-id="292f0-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="292f0-124">RELATED LINKS</span></span>
