---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112576"
---
# <span data-ttu-id="c56ae-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c56ae-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="c56ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c56ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c56ae-103">Remova uma ou várias configurações de Malha de Serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="c56ae-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="c56ae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c56ae-104">SYNTAX</span></span>

### <span data-ttu-id="c56ae-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="c56ae-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56ae-106">LotesConjunto</span><span class="sxs-lookup"><span data-stu-id="c56ae-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56ae-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c56ae-107">DESCRIPTION</span></span>
<span data-ttu-id="c56ae-108">Use **Remove-AzServiceFabricSetting** para remover as configurações de Malha de Serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="c56ae-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="c56ae-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c56ae-109">EXAMPLES</span></span>

### <span data-ttu-id="c56ae-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c56ae-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="c56ae-111">Esse comando removerá as configurações "MaxCursors" na seção "EseStore".</span><span class="sxs-lookup"><span data-stu-id="c56ae-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="c56ae-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c56ae-112">PARAMETERS</span></span>

### <span data-ttu-id="c56ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56ae-113">-DefaultProfile</span></span>
<span data-ttu-id="c56ae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c56ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56ae-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c56ae-115">-Name</span></span>
<span data-ttu-id="c56ae-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="c56ae-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c56ae-117">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c56ae-117">-Parameter</span></span>
<span data-ttu-id="c56ae-118">Nome do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="c56ae-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="c56ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="c56ae-120">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c56ae-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c56ae-121">-Seção</span><span class="sxs-lookup"><span data-stu-id="c56ae-121">-Section</span></span>
<span data-ttu-id="c56ae-122">Nome da seção da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="c56ae-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="c56ae-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="c56ae-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="c56ae-124">Uma matriz de configurações de malha</span><span class="sxs-lookup"><span data-stu-id="c56ae-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="c56ae-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c56ae-125">-Confirm</span></span>
<span data-ttu-id="c56ae-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c56ae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56ae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56ae-127">-WhatIf</span></span>
<span data-ttu-id="c56ae-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c56ae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56ae-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c56ae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56ae-130">CommonParameters</span></span>
<span data-ttu-id="c56ae-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56ae-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c56ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56ae-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="c56ae-133">INPUTS</span></span>

### <span data-ttu-id="c56ae-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c56ae-134">System.String</span></span>

### <span data-ttu-id="c56ae-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="c56ae-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="c56ae-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="c56ae-136">OUTPUTS</span></span>

### <span data-ttu-id="c56ae-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="c56ae-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c56ae-138">Notas</span><span class="sxs-lookup"><span data-stu-id="c56ae-138">NOTES</span></span>

## <span data-ttu-id="c56ae-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c56ae-139">RELATED LINKS</span></span>
