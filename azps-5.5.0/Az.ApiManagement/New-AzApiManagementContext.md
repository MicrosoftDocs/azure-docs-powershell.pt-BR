---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115570"
---
# <span data-ttu-id="bb241-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb241-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="bb241-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb241-102">SYNOPSIS</span></span>
<span data-ttu-id="bb241-103">Cria uma instância do PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bb241-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="bb241-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb241-104">SYNTAX</span></span>

### <span data-ttu-id="bb241-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb241-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb241-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb241-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb241-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb241-107">DESCRIPTION</span></span>
<span data-ttu-id="bb241-108">O cmdlet **New-AzApiManagementContext cria** uma instância **de PsAzureApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="bb241-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="bb241-109">O contexto é usado para todos os cmdlets de serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="bb241-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="bb241-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb241-110">EXAMPLES</span></span>

### <span data-ttu-id="bb241-111">Exemplo 1: Criar uma instância PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb241-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="bb241-112">Esse comando cria uma instância **de PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="bb241-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="bb241-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb241-113">PARAMETERS</span></span>

### <span data-ttu-id="bb241-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb241-114">-DefaultProfile</span></span>
<span data-ttu-id="bb241-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bb241-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb241-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb241-116">-ResourceGroupName</span></span>
<span data-ttu-id="bb241-117">Especifica o nome do grupo de recursos no qual um serviço de Gerenciamento de API é implantado.</span><span class="sxs-lookup"><span data-stu-id="bb241-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="bb241-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb241-118">-ResourceId</span></span>
<span data-ttu-id="bb241-119">Identificador de Recursos Arm de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="bb241-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="bb241-120">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="bb241-120">This parameter is required.</span></span>

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

### <span data-ttu-id="bb241-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bb241-121">-ServiceName</span></span>
<span data-ttu-id="bb241-122">Especifica o nome do serviço de Gerenciamento de API implantado.</span><span class="sxs-lookup"><span data-stu-id="bb241-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="bb241-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb241-123">CommonParameters</span></span>
<span data-ttu-id="bb241-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb241-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb241-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb241-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb241-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb241-126">INPUTS</span></span>

### <span data-ttu-id="bb241-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bb241-127">System.String</span></span>

## <span data-ttu-id="bb241-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb241-128">OUTPUTS</span></span>

### <span data-ttu-id="bb241-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb241-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="bb241-130">Notas</span><span class="sxs-lookup"><span data-stu-id="bb241-130">NOTES</span></span>

## <span data-ttu-id="bb241-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb241-131">RELATED LINKS</span></span>
