---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126187"
---
# <span data-ttu-id="7c42c-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="7c42c-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="7c42c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c42c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c42c-103">Defina os módulos de borda em um único dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="7c42c-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="7c42c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c42c-104">SYNTAX</span></span>

### <span data-ttu-id="7c42c-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7c42c-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c42c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c42c-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c42c-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="7c42c-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c42c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c42c-108">DESCRIPTION</span></span>
<span data-ttu-id="7c42c-109">Aplica o conteúdo de configuração dos módulos fornecidos ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="7c42c-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="7c42c-110">Observação: após a execução, o comando produzirá a coleção de módulos aplicados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c42c-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="7c42c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c42c-111">EXAMPLES</span></span>

### <span data-ttu-id="7c42c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c42c-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="7c42c-113">Testar módulos Edge durante o desenvolvimento definindo módulos em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="7c42c-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="7c42c-114">OS</span><span class="sxs-lookup"><span data-stu-id="7c42c-114">PARAMETERS</span></span>

### <span data-ttu-id="7c42c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c42c-115">-DefaultProfile</span></span>
<span data-ttu-id="7c42c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c42c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c42c-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="7c42c-117">-DeviceId</span></span>
<span data-ttu-id="7c42c-118">ID do dispositivo de borda de destino.</span><span class="sxs-lookup"><span data-stu-id="7c42c-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="7c42c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c42c-119">-InputObject</span></span>
<span data-ttu-id="7c42c-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7c42c-120">IotHub object</span></span>

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

### <span data-ttu-id="7c42c-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7c42c-121">-IotHubName</span></span>
<span data-ttu-id="7c42c-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="7c42c-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7c42c-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="7c42c-123">-ModulesContent</span></span>
<span data-ttu-id="7c42c-124">Conteúdo de configuração de módulos para dispositivos de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="7c42c-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="7c42c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c42c-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c42c-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7c42c-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c42c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c42c-127">-ResourceId</span></span>
<span data-ttu-id="7c42c-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7c42c-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7c42c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c42c-129">-Confirm</span></span>
<span data-ttu-id="7c42c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c42c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c42c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c42c-131">-WhatIf</span></span>
<span data-ttu-id="7c42c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c42c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c42c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c42c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c42c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c42c-134">CommonParameters</span></span>
<span data-ttu-id="7c42c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c42c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c42c-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c42c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c42c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c42c-137">INPUTS</span></span>

### <span data-ttu-id="7c42c-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7c42c-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7c42c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7c42c-139">System.String</span></span>

## <span data-ttu-id="7c42c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c42c-140">OUTPUTS</span></span>

### <span data-ttu-id="7c42c-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="7c42c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="7c42c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c42c-142">NOTES</span></span>

## <span data-ttu-id="7c42c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c42c-143">RELATED LINKS</span></span>
