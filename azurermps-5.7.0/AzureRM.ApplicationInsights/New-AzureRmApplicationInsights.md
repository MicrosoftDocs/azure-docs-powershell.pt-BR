---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 23c79f4ceed4e6b9dc537cb6e04fb602fd7a4bbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602876"
---
# <span data-ttu-id="f9a5d-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f9a5d-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="f9a5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a5d-103">Criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="f9a5d-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9a5d-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9a5d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a5d-106">Criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="f9a5d-106">Create a new application insights resource</span></span>

## <span data-ttu-id="f9a5d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a5d-108">Exemplo 1 criar um novo recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="f9a5d-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
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

<span data-ttu-id="f9a5d-109">Adicione um novo recurso do Application insights chamado "Test" no grupo de recursos "grupo de teste" com o tipo "Java".</span><span class="sxs-lookup"><span data-stu-id="f9a5d-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="f9a5d-110">OS</span><span class="sxs-lookup"><span data-stu-id="f9a5d-110">PARAMETERS</span></span>

### <span data-ttu-id="f9a5d-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9a5d-111">-Confirm</span></span>
<span data-ttu-id="f9a5d-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a5d-113">-DefaultProfile</span></span>
<span data-ttu-id="f9a5d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-115">-Kind</span><span class="sxs-lookup"><span data-stu-id="f9a5d-115">-Kind</span></span>
<span data-ttu-id="f9a5d-116">Tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-116">Application kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-117">-Local</span><span class="sxs-lookup"><span data-stu-id="f9a5d-117">-Location</span></span>
<span data-ttu-id="f9a5d-118">Localização de recursos do Application insights.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-118">Application Insights Resource Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9a5d-119">-Name</span></span>
<span data-ttu-id="f9a5d-120">Nome do recurso do Application insights.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-120">Application Insights Resource Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a5d-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9a5d-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="f9a5d-123">-Tag</span></span>
<span data-ttu-id="f9a5d-124">Marcas de componente.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-124">Component Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a5d-125">-WhatIf</span></span>
<span data-ttu-id="f9a5d-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9a5d-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a5d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a5d-128">CommonParameters</span></span>
<span data-ttu-id="f9a5d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a5d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a5d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a5d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9a5d-131">INPUTS</span></span>

### <span data-ttu-id="f9a5d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f9a5d-132">System.String</span></span>

## <span data-ttu-id="f9a5d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9a5d-133">OUTPUTS</span></span>

### <span data-ttu-id="f9a5d-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f9a5d-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f9a5d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9a5d-135">NOTES</span></span>

## <span data-ttu-id="f9a5d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9a5d-136">RELATED LINKS</span></span>

