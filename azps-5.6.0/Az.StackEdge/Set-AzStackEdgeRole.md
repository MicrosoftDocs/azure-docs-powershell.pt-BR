---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 5a6828231b276fc698179d78d3ae4bda7a4c6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885252"
---
# <span data-ttu-id="bf907-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="bf907-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="bf907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf907-102">SYNOPSIS</span></span>
<span data-ttu-id="bf907-103">Atualiza uma função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="bf907-103">Updates a Role for a device</span></span>

## <span data-ttu-id="bf907-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bf907-104">SYNTAX</span></span>

### <span data-ttu-id="bf907-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bf907-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf907-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf907-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf907-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf907-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf907-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bf907-108">DESCRIPTION</span></span>
<span data-ttu-id="bf907-109">O cmdlet **Set-AzStackEdgeRole** atualiza uma função de IoT para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="bf907-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="bf907-110">Os compartilhamentos montados antigos serão substituídos por os recém-fornecidos no parâmetro ShareName.</span><span class="sxs-lookup"><span data-stu-id="bf907-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="bf907-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf907-111">EXAMPLES</span></span>

### <span data-ttu-id="bf907-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf907-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="bf907-113">Nomes de Compartilhamento substituirão os compartilhamentos montados antigos com os recém-fornecidos</span><span class="sxs-lookup"><span data-stu-id="bf907-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="bf907-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf907-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="bf907-115">Para desmontar todas as compartilhamentos</span><span class="sxs-lookup"><span data-stu-id="bf907-115">To unmount all shares</span></span>

## <span data-ttu-id="bf907-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bf907-116">PARAMETERS</span></span>

### <span data-ttu-id="bf907-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf907-117">-DefaultProfile</span></span>
<span data-ttu-id="bf907-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf907-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf907-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bf907-119">-DeviceName</span></span>
<span data-ttu-id="bf907-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="bf907-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf907-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf907-121">-InputObject</span></span>
<span data-ttu-id="bf907-122">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="bf907-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf907-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bf907-123">-Name</span></span>
<span data-ttu-id="bf907-124">Nome da função</span><span class="sxs-lookup"><span data-stu-id="bf907-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf907-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf907-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf907-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bf907-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf907-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf907-127">-ResourceId</span></span>
<span data-ttu-id="bf907-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf907-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf907-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bf907-129">-ShareName</span></span>
<span data-ttu-id="bf907-130">Share(s) in a role</span><span class="sxs-lookup"><span data-stu-id="bf907-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf907-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf907-131">-Confirm</span></span>
<span data-ttu-id="bf907-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf907-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf907-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf907-133">-WhatIf</span></span>
<span data-ttu-id="bf907-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf907-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf907-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf907-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf907-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf907-136">CommonParameters</span></span>
<span data-ttu-id="bf907-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf907-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf907-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf907-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf907-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf907-139">INPUTS</span></span>

### <span data-ttu-id="bf907-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bf907-140">System.String</span></span>

### <span data-ttu-id="bf907-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="bf907-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="bf907-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bf907-142">OUTPUTS</span></span>

### <span data-ttu-id="bf907-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="bf907-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="bf907-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="bf907-144">NOTES</span></span>

## <span data-ttu-id="bf907-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf907-145">RELATED LINKS</span></span>
