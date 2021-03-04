---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: f3bc819c7050300c82f039981b1df34010771eb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885464"
---
# <span data-ttu-id="17679-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="17679-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="17679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17679-102">SYNOPSIS</span></span>
<span data-ttu-id="17679-103">Definir módulos de borda em um único dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="17679-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="17679-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17679-104">SYNTAX</span></span>

### <span data-ttu-id="17679-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17679-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17679-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17679-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17679-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="17679-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17679-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17679-108">DESCRIPTION</span></span>
<span data-ttu-id="17679-109">Aplica o conteúdo de configuração de módulos fornecidos ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="17679-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="17679-110">Observação: após a execução, o comando dará o resultado da coleção de módulos aplicados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17679-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="17679-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17679-111">EXAMPLES</span></span>

### <span data-ttu-id="17679-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17679-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="17679-113">Teste módulos de borda durante o desenvolvimento definindo módulos em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="17679-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="17679-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17679-114">PARAMETERS</span></span>

### <span data-ttu-id="17679-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17679-115">-DefaultProfile</span></span>
<span data-ttu-id="17679-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17679-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17679-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="17679-117">-DeviceId</span></span>
<span data-ttu-id="17679-118">ID do Dispositivo de Borda de Destino.</span><span class="sxs-lookup"><span data-stu-id="17679-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="17679-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17679-119">-InputObject</span></span>
<span data-ttu-id="17679-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="17679-120">IotHub object</span></span>

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

### <span data-ttu-id="17679-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="17679-121">-IotHubName</span></span>
<span data-ttu-id="17679-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="17679-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="17679-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="17679-123">-ModulesContent</span></span>
<span data-ttu-id="17679-124">Conteúdo de configuração de módulos para dispositivos de Borda IoT.</span><span class="sxs-lookup"><span data-stu-id="17679-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="17679-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17679-125">-ResourceGroupName</span></span>
<span data-ttu-id="17679-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="17679-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="17679-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17679-127">-ResourceId</span></span>
<span data-ttu-id="17679-128">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="17679-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="17679-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17679-129">-Confirm</span></span>
<span data-ttu-id="17679-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17679-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17679-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17679-131">-WhatIf</span></span>
<span data-ttu-id="17679-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17679-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17679-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17679-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17679-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17679-134">CommonParameters</span></span>
<span data-ttu-id="17679-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17679-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17679-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17679-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17679-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17679-137">INPUTS</span></span>

### <span data-ttu-id="17679-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="17679-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="17679-139">System.String</span><span class="sxs-lookup"><span data-stu-id="17679-139">System.String</span></span>

## <span data-ttu-id="17679-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17679-140">OUTPUTS</span></span>

### <span data-ttu-id="17679-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="17679-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="17679-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="17679-142">NOTES</span></span>

## <span data-ttu-id="17679-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17679-143">RELATED LINKS</span></span>
