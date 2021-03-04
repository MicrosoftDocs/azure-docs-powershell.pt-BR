---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: b7124b00452637ca3e496a0417745ee7719278e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888587"
---
# <span data-ttu-id="9d51e-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d51e-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="9d51e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d51e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d51e-103">Cria uma instância de PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9d51e-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="9d51e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9d51e-104">SYNTAX</span></span>

### <span data-ttu-id="9d51e-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9d51e-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d51e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51e-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d51e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9d51e-107">DESCRIPTION</span></span>
<span data-ttu-id="9d51e-108">O cmdlet **New-AzApiManagementContext** cria uma instância de **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="9d51e-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="9d51e-109">O contexto é usado para todos os cmdlets do serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="9d51e-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="9d51e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d51e-110">EXAMPLES</span></span>

### <span data-ttu-id="9d51e-111">Exemplo 1: Criar uma instância PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d51e-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="9d51e-112">Este comando cria uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="9d51e-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="9d51e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9d51e-113">PARAMETERS</span></span>

### <span data-ttu-id="9d51e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d51e-114">-DefaultProfile</span></span>
<span data-ttu-id="9d51e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9d51e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d51e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d51e-116">-ResourceGroupName</span></span>
<span data-ttu-id="9d51e-117">Especifica o nome do grupo de recursos no qual um serviço de Gerenciamento de API é implantado.</span><span class="sxs-lookup"><span data-stu-id="9d51e-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d51e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d51e-118">-ResourceId</span></span>
<span data-ttu-id="9d51e-119">Identificador de Recurso arm de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9d51e-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="9d51e-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="9d51e-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d51e-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9d51e-121">-ServiceName</span></span>
<span data-ttu-id="9d51e-122">Especifica o nome do serviço de Gerenciamento de API implantado.</span><span class="sxs-lookup"><span data-stu-id="9d51e-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d51e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d51e-123">CommonParameters</span></span>
<span data-ttu-id="9d51e-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d51e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d51e-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d51e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d51e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d51e-126">INPUTS</span></span>

### <span data-ttu-id="9d51e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9d51e-127">System.String</span></span>

## <span data-ttu-id="9d51e-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9d51e-128">OUTPUTS</span></span>

### <span data-ttu-id="9d51e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d51e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9d51e-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="9d51e-130">NOTES</span></span>

## <span data-ttu-id="9d51e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d51e-131">RELATED LINKS</span></span>
