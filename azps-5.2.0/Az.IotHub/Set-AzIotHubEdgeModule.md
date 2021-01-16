---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261869"
---
# <span data-ttu-id="9ca6a-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="9ca6a-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="9ca6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ca6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca6a-103">Defina os módulos de borda em um único dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="9ca6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ca6a-104">SYNTAX</span></span>

### <span data-ttu-id="9ca6a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ca6a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca6a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ca6a-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca6a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="9ca6a-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca6a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ca6a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca6a-109">Aplica o conteúdo de configuração dos módulos fornecidos ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="9ca6a-110">Observação: após a execução, o comando produzirá a coleção de módulos aplicados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="9ca6a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ca6a-111">EXAMPLES</span></span>

### <span data-ttu-id="9ca6a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ca6a-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="9ca6a-113">Testar módulos Edge durante o desenvolvimento definindo módulos em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="9ca6a-114">OS</span><span class="sxs-lookup"><span data-stu-id="9ca6a-114">PARAMETERS</span></span>

### <span data-ttu-id="9ca6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca6a-115">-DefaultProfile</span></span>
<span data-ttu-id="9ca6a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca6a-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="9ca6a-117">-DeviceId</span></span>
<span data-ttu-id="9ca6a-118">ID do dispositivo de borda de destino.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="9ca6a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca6a-119">-InputObject</span></span>
<span data-ttu-id="9ca6a-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="9ca6a-120">IotHub object</span></span>

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

### <span data-ttu-id="9ca6a-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9ca6a-121">-IotHubName</span></span>
<span data-ttu-id="9ca6a-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="9ca6a-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9ca6a-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="9ca6a-123">-ModulesContent</span></span>
<span data-ttu-id="9ca6a-124">Conteúdo de configuração de módulos para dispositivos de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="9ca6a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca6a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9ca6a-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9ca6a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ca6a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca6a-127">-ResourceId</span></span>
<span data-ttu-id="9ca6a-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="9ca6a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9ca6a-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ca6a-129">-Confirm</span></span>
<span data-ttu-id="9ca6a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca6a-131">-WhatIf</span></span>
<span data-ttu-id="9ca6a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca6a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca6a-134">CommonParameters</span></span>
<span data-ttu-id="9ca6a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca6a-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca6a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca6a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ca6a-137">INPUTS</span></span>

### <span data-ttu-id="9ca6a-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9ca6a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9ca6a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ca6a-139">System.String</span></span>

## <span data-ttu-id="9ca6a-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ca6a-140">OUTPUTS</span></span>

### <span data-ttu-id="9ca6a-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="9ca6a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="9ca6a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ca6a-142">NOTES</span></span>

## <span data-ttu-id="9ca6a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ca6a-143">RELATED LINKS</span></span>
