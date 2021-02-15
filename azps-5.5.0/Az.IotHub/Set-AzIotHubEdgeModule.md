---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111843"
---
# <span data-ttu-id="76fc0-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="76fc0-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="76fc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="76fc0-103">Definir módulos de borda em um único dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="76fc0-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="76fc0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76fc0-104">SYNTAX</span></span>

### <span data-ttu-id="76fc0-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76fc0-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76fc0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76fc0-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fc0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="76fc0-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76fc0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="76fc0-108">DESCRIPTION</span></span>
<span data-ttu-id="76fc0-109">Aplica o conteúdo de configuração de módulos fornecidos ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="76fc0-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="76fc0-110">Observação: após a execução, o comando saída do conjunto de módulos aplicados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76fc0-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="76fc0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76fc0-111">EXAMPLES</span></span>

### <span data-ttu-id="76fc0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76fc0-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="76fc0-113">Teste módulos de borda enquanto estiver em desenvolvimento definindo módulos em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="76fc0-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="76fc0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76fc0-114">PARAMETERS</span></span>

### <span data-ttu-id="76fc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fc0-115">-DefaultProfile</span></span>
<span data-ttu-id="76fc0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76fc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fc0-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="76fc0-117">-DeviceId</span></span>
<span data-ttu-id="76fc0-118">ID do Dispositivo de Borda de Destino.</span><span class="sxs-lookup"><span data-stu-id="76fc0-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fc0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76fc0-119">-InputObject</span></span>
<span data-ttu-id="76fc0-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="76fc0-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76fc0-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="76fc0-121">-IotHubName</span></span>
<span data-ttu-id="76fc0-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="76fc0-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fc0-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="76fc0-123">-ModulesContent</span></span>
<span data-ttu-id="76fc0-124">Conteúdo de configuração de módulos para dispositivos de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="76fc0-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="76fc0-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="76fc0-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fc0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76fc0-127">-ResourceId</span></span>
<span data-ttu-id="76fc0-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="76fc0-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76fc0-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76fc0-129">-Confirm</span></span>
<span data-ttu-id="76fc0-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76fc0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fc0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fc0-131">-WhatIf</span></span>
<span data-ttu-id="76fc0-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76fc0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76fc0-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76fc0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fc0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fc0-134">CommonParameters</span></span>
<span data-ttu-id="76fc0-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fc0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fc0-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76fc0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fc0-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="76fc0-137">INPUTS</span></span>

### <span data-ttu-id="76fc0-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="76fc0-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="76fc0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="76fc0-139">System.String</span></span>

## <span data-ttu-id="76fc0-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="76fc0-140">OUTPUTS</span></span>

### <span data-ttu-id="76fc0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="76fc0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="76fc0-142">Notas</span><span class="sxs-lookup"><span data-stu-id="76fc0-142">NOTES</span></span>

## <span data-ttu-id="76fc0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76fc0-143">RELATED LINKS</span></span>
