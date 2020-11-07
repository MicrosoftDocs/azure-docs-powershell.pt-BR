---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 550fb398dbd636ba9c43c66d31b78384610cf42b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944147"
---
# <span data-ttu-id="28f75-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="28f75-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="28f75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28f75-102">SYNOPSIS</span></span>
<span data-ttu-id="28f75-103">Criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="28f75-103">Create a new application insights resource</span></span>

## <span data-ttu-id="28f75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28f75-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28f75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28f75-105">DESCRIPTION</span></span>
<span data-ttu-id="28f75-106">Criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="28f75-106">Create a new application insights resource</span></span>

## <span data-ttu-id="28f75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28f75-107">EXAMPLES</span></span>

### <span data-ttu-id="28f75-108">Exemplo 1 criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="28f75-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
```

<span data-ttu-id="28f75-109">Adicione um novo recurso do Application insights chamado "Test" no grupo de recursos "grupo de teste" com o tipo "Java".</span><span class="sxs-lookup"><span data-stu-id="28f75-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="28f75-110">OS</span><span class="sxs-lookup"><span data-stu-id="28f75-110">PARAMETERS</span></span>

### <span data-ttu-id="28f75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f75-111">-DefaultProfile</span></span>
<span data-ttu-id="28f75-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28f75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28f75-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="28f75-113">-Kind</span></span>
<span data-ttu-id="28f75-114">Tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28f75-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-115">-Local</span><span class="sxs-lookup"><span data-stu-id="28f75-115">-Location</span></span>
<span data-ttu-id="28f75-116">Localização de recursos do Application insights.</span><span class="sxs-lookup"><span data-stu-id="28f75-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="28f75-117">-Name</span></span>
<span data-ttu-id="28f75-118">Nome do recurso do Application insights.</span><span class="sxs-lookup"><span data-stu-id="28f75-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f75-119">-ResourceGroupName</span></span>
<span data-ttu-id="28f75-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28f75-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="28f75-121">-Tag</span></span>
<span data-ttu-id="28f75-122">Marcas de componente.</span><span class="sxs-lookup"><span data-stu-id="28f75-122">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28f75-123">-Confirm</span></span>
<span data-ttu-id="28f75-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28f75-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f75-125">-WhatIf</span></span>
<span data-ttu-id="28f75-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28f75-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28f75-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28f75-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f75-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f75-128">CommonParameters</span></span>
<span data-ttu-id="28f75-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f75-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f75-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f75-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f75-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28f75-131">INPUTS</span></span>

### <span data-ttu-id="28f75-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="28f75-132">None</span></span>

## <span data-ttu-id="28f75-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28f75-133">OUTPUTS</span></span>

### <span data-ttu-id="28f75-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="28f75-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="28f75-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28f75-135">NOTES</span></span>

## <span data-ttu-id="28f75-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28f75-136">RELATED LINKS</span></span>
