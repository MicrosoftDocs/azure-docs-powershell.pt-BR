---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 22dee84aadc590d140d64cbd71eeaed3c16f03e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775923"
---
# <span data-ttu-id="03b11-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="03b11-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="03b11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03b11-102">SYNOPSIS</span></span>
<span data-ttu-id="03b11-103">Atualiza uma função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="03b11-103">Updates a Role for a device</span></span>

## <span data-ttu-id="03b11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03b11-104">SYNTAX</span></span>

### <span data-ttu-id="03b11-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="03b11-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b11-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03b11-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b11-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03b11-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b11-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03b11-108">DESCRIPTION</span></span>
<span data-ttu-id="03b11-109">O cmdlet **set-AzDataBoxEdgeRole** atualiza uma função IOT para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="03b11-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="03b11-110">Os antigos compartilhamentos montados serão substituídos pelos recém fornecidos no parâmetro ShareName.</span><span class="sxs-lookup"><span data-stu-id="03b11-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="03b11-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03b11-111">EXAMPLES</span></span>

### <span data-ttu-id="03b11-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03b11-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="03b11-113">Os nomes de compartilhamento substituirão os compartilhamentos montados antigos pelos novos fornecidos</span><span class="sxs-lookup"><span data-stu-id="03b11-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="03b11-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="03b11-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="03b11-115">Para desmontar todos os compartilhamentos</span><span class="sxs-lookup"><span data-stu-id="03b11-115">To unmount all shares</span></span>

## <span data-ttu-id="03b11-116">OS</span><span class="sxs-lookup"><span data-stu-id="03b11-116">PARAMETERS</span></span>

### <span data-ttu-id="03b11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b11-117">-DefaultProfile</span></span>
<span data-ttu-id="03b11-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03b11-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03b11-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="03b11-119">-DeviceName</span></span>
<span data-ttu-id="03b11-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="03b11-120">Device Name</span></span>

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

### <span data-ttu-id="03b11-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03b11-121">-InputObject</span></span>
<span data-ttu-id="03b11-122">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="03b11-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03b11-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="03b11-123">-Name</span></span>
<span data-ttu-id="03b11-124">Nome da função</span><span class="sxs-lookup"><span data-stu-id="03b11-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b11-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b11-125">-ResourceGroupName</span></span>
<span data-ttu-id="03b11-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="03b11-126">Resource Group Name</span></span>

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

### <span data-ttu-id="03b11-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03b11-127">-ResourceId</span></span>
<span data-ttu-id="03b11-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="03b11-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="03b11-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="03b11-129">-ShareName</span></span>
<span data-ttu-id="03b11-130">Compartilhamento (s) em uma função</span><span class="sxs-lookup"><span data-stu-id="03b11-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b11-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03b11-131">-Confirm</span></span>
<span data-ttu-id="03b11-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b11-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b11-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b11-133">-WhatIf</span></span>
<span data-ttu-id="03b11-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03b11-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03b11-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03b11-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b11-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b11-136">CommonParameters</span></span>
<span data-ttu-id="03b11-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b11-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b11-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03b11-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b11-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03b11-139">INPUTS</span></span>

### <span data-ttu-id="03b11-140">System. String</span><span class="sxs-lookup"><span data-stu-id="03b11-140">System.String</span></span>

### <span data-ttu-id="03b11-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="03b11-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="03b11-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03b11-142">OUTPUTS</span></span>

### <span data-ttu-id="03b11-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="03b11-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="03b11-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03b11-144">NOTES</span></span>

## <span data-ttu-id="03b11-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03b11-145">RELATED LINKS</span></span>