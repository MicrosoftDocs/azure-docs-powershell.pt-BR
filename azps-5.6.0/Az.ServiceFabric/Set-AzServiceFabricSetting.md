---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888427"
---
# <span data-ttu-id="bf556-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="bf556-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="bf556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf556-102">SYNOPSIS</span></span>
<span data-ttu-id="bf556-103">Adicione ou atualize uma ou várias configurações do Service Fabric ao cluster.</span><span class="sxs-lookup"><span data-stu-id="bf556-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="bf556-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bf556-104">SYNTAX</span></span>

### <span data-ttu-id="bf556-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="bf556-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf556-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="bf556-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf556-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bf556-107">DESCRIPTION</span></span>
<span data-ttu-id="bf556-108">Use **Set-AzServiceFabricSetting** para adicionar ou atualizar configurações do Service Fabric em um cluster.</span><span class="sxs-lookup"><span data-stu-id="bf556-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="bf556-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf556-109">EXAMPLES</span></span>

### <span data-ttu-id="bf556-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf556-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="bf556-111">Este comando definirá 'MaxFileOperationTimeout' como valor '5000' na seção 'NomingService'.</span><span class="sxs-lookup"><span data-stu-id="bf556-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="bf556-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf556-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="bf556-113">Este comando disparará uma atualização para definir várias configurações de malha usando o parâmetro SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="bf556-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="bf556-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bf556-114">PARAMETERS</span></span>

### <span data-ttu-id="bf556-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf556-115">-DefaultProfile</span></span>
<span data-ttu-id="bf556-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf556-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf556-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bf556-117">-Name</span></span>
<span data-ttu-id="bf556-118">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="bf556-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf556-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="bf556-119">-Parameter</span></span>
<span data-ttu-id="bf556-120">Nome do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="bf556-120">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf556-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf556-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf556-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf556-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf556-123">-Section</span><span class="sxs-lookup"><span data-stu-id="bf556-123">-Section</span></span>
<span data-ttu-id="bf556-124">Nome da seção da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="bf556-124">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf556-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="bf556-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="bf556-126">Uma matriz de configurações de malha</span><span class="sxs-lookup"><span data-stu-id="bf556-126">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf556-127">-Value</span><span class="sxs-lookup"><span data-stu-id="bf556-127">-Value</span></span>
<span data-ttu-id="bf556-128">Valor do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="bf556-128">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf556-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf556-129">-Confirm</span></span>
<span data-ttu-id="bf556-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf556-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf556-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf556-131">-WhatIf</span></span>
<span data-ttu-id="bf556-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf556-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf556-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf556-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf556-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf556-134">CommonParameters</span></span>
<span data-ttu-id="bf556-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf556-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf556-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf556-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf556-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf556-137">INPUTS</span></span>

### <span data-ttu-id="bf556-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bf556-138">System.String</span></span>

### <span data-ttu-id="bf556-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="bf556-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="bf556-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bf556-140">OUTPUTS</span></span>

### <span data-ttu-id="bf556-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="bf556-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bf556-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="bf556-142">NOTES</span></span>

## <span data-ttu-id="bf556-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf556-143">RELATED LINKS</span></span>
