---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943897"
---
# <span data-ttu-id="3d75a-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3d75a-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="3d75a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d75a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d75a-103">Atualiza uma função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d75a-103">Updates a Role for a device</span></span>

## <span data-ttu-id="3d75a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d75a-104">SYNTAX</span></span>

### <span data-ttu-id="3d75a-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d75a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d75a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d75a-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d75a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d75a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d75a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d75a-108">DESCRIPTION</span></span>
<span data-ttu-id="3d75a-109">O cmdlet **set-AzStackEdgeRole** atualiza uma função IOT para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="3d75a-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="3d75a-110">Os antigos compartilhamentos montados serão substituídos pelos recém fornecidos no parâmetro ShareName.</span><span class="sxs-lookup"><span data-stu-id="3d75a-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="3d75a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d75a-111">EXAMPLES</span></span>

### <span data-ttu-id="3d75a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d75a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="3d75a-113">Os nomes de compartilhamento substituirão os compartilhamentos montados antigos pelos novos fornecidos</span><span class="sxs-lookup"><span data-stu-id="3d75a-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="3d75a-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d75a-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="3d75a-115">Para desmontar todos os compartilhamentos</span><span class="sxs-lookup"><span data-stu-id="3d75a-115">To unmount all shares</span></span>

## <span data-ttu-id="3d75a-116">OS</span><span class="sxs-lookup"><span data-stu-id="3d75a-116">PARAMETERS</span></span>

### <span data-ttu-id="3d75a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d75a-117">-DefaultProfile</span></span>
<span data-ttu-id="3d75a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d75a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d75a-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3d75a-119">-DeviceName</span></span>
<span data-ttu-id="3d75a-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d75a-120">Device Name</span></span>

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

### <span data-ttu-id="3d75a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d75a-121">-InputObject</span></span>
<span data-ttu-id="3d75a-122">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="3d75a-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3d75a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d75a-123">-Name</span></span>
<span data-ttu-id="3d75a-124">Nome da função</span><span class="sxs-lookup"><span data-stu-id="3d75a-124">Name of the Role</span></span>

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

### <span data-ttu-id="3d75a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d75a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3d75a-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3d75a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3d75a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d75a-127">-ResourceId</span></span>
<span data-ttu-id="3d75a-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="3d75a-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="3d75a-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3d75a-129">-ShareName</span></span>
<span data-ttu-id="3d75a-130">Compartilhamento (s) em uma função</span><span class="sxs-lookup"><span data-stu-id="3d75a-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="3d75a-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d75a-131">-Confirm</span></span>
<span data-ttu-id="3d75a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d75a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d75a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d75a-133">-WhatIf</span></span>
<span data-ttu-id="3d75a-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d75a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d75a-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d75a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d75a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d75a-136">CommonParameters</span></span>
<span data-ttu-id="3d75a-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d75a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d75a-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d75a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d75a-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d75a-139">INPUTS</span></span>

### <span data-ttu-id="3d75a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3d75a-140">System.String</span></span>

### <span data-ttu-id="3d75a-141">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3d75a-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3d75a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d75a-142">OUTPUTS</span></span>

### <span data-ttu-id="3d75a-143">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3d75a-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3d75a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d75a-144">NOTES</span></span>

## <span data-ttu-id="3d75a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d75a-145">RELATED LINKS</span></span>
