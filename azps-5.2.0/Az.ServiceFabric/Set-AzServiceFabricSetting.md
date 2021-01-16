---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262977"
---
# <span data-ttu-id="31909-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="31909-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="31909-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31909-102">SYNOPSIS</span></span>
<span data-ttu-id="31909-103">Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.</span><span class="sxs-lookup"><span data-stu-id="31909-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="31909-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31909-104">SYNTAX</span></span>

### <span data-ttu-id="31909-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="31909-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31909-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="31909-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31909-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31909-107">DESCRIPTION</span></span>
<span data-ttu-id="31909-108">Use **set-AzServiceFabricSetting** para adicionar ou atualizar as configurações do Service Fabric em um cluster.</span><span class="sxs-lookup"><span data-stu-id="31909-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="31909-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31909-109">EXAMPLES</span></span>

### <span data-ttu-id="31909-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31909-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="31909-111">Esse comando definirá ' MaxFileOperationTimeout ' como o valor ' 5000 ' na seção ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="31909-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="31909-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="31909-112">Example 2</span></span>
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

<span data-ttu-id="31909-113">Esse comando irá disparar uma atualização para definir várias configurações de malha usando o parâmetro SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="31909-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="31909-114">OS</span><span class="sxs-lookup"><span data-stu-id="31909-114">PARAMETERS</span></span>

### <span data-ttu-id="31909-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31909-115">-DefaultProfile</span></span>
<span data-ttu-id="31909-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31909-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31909-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31909-117">-Name</span></span>
<span data-ttu-id="31909-118">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="31909-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="31909-119">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="31909-119">-Parameter</span></span>
<span data-ttu-id="31909-120">Nome do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="31909-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="31909-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31909-121">-ResourceGroupName</span></span>
<span data-ttu-id="31909-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31909-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="31909-123">-Seção</span><span class="sxs-lookup"><span data-stu-id="31909-123">-Section</span></span>
<span data-ttu-id="31909-124">Nome da seção da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="31909-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="31909-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="31909-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="31909-126">Uma matriz de configurações da malha</span><span class="sxs-lookup"><span data-stu-id="31909-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="31909-127">-Valor</span><span class="sxs-lookup"><span data-stu-id="31909-127">-Value</span></span>
<span data-ttu-id="31909-128">Valor do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="31909-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="31909-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31909-129">-Confirm</span></span>
<span data-ttu-id="31909-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31909-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31909-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31909-131">-WhatIf</span></span>
<span data-ttu-id="31909-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31909-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31909-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31909-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31909-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31909-134">CommonParameters</span></span>
<span data-ttu-id="31909-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31909-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31909-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31909-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31909-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31909-137">INPUTS</span></span>

### <span data-ttu-id="31909-138">System. String</span><span class="sxs-lookup"><span data-stu-id="31909-138">System.String</span></span>

### <span data-ttu-id="31909-139">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="31909-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="31909-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31909-140">OUTPUTS</span></span>

### <span data-ttu-id="31909-141">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="31909-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="31909-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31909-142">NOTES</span></span>

## <span data-ttu-id="31909-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31909-143">RELATED LINKS</span></span>
