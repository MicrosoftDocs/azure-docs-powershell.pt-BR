---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943426"
---
# <span data-ttu-id="9ec78-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9ec78-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9ec78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ec78-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec78-103">Obtém as informações sobre dispositivos de borda de caixa de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9ec78-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="9ec78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ec78-104">SYNTAX</span></span>

### <span data-ttu-id="9ec78-105">ListByParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ec78-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec78-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec78-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec78-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec78-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec78-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ec78-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec78-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec78-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec78-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec78-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ec78-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ec78-116">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ec78-116">DESCRIPTION</span></span>
<span data-ttu-id="9ec78-117">O cmdlet **Get-AzDataBoxEdgeDevice** Obtém as informações sobre os dispositivos de borda da caixa de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9ec78-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="9ec78-118">Você pode especificar o nome do dispositivo juntamente com o nome do grupo de recursos para obter as informações em um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="9ec78-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="9ec78-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ec78-119">EXAMPLES</span></span>

### <span data-ttu-id="9ec78-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ec78-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="9ec78-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9ec78-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="9ec78-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9ec78-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="9ec78-123">OS</span><span class="sxs-lookup"><span data-stu-id="9ec78-123">PARAMETERS</span></span>

### <span data-ttu-id="9ec78-124">-Alerta</span><span class="sxs-lookup"><span data-stu-id="9ec78-124">-Alert</span></span>
<span data-ttu-id="9ec78-125">Buscar os alertas na caixa de dados dispositivo de borda/gateway</span><span class="sxs-lookup"><span data-stu-id="9ec78-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec78-126">-DefaultProfile</span></span>
<span data-ttu-id="9ec78-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ec78-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ec78-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="9ec78-128">-ExtendedInfo</span></span>
<span data-ttu-id="9ec78-129">Obtém informações adicionais para o dispositivo de gateway de caixa de dados de borda/caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="9ec78-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ec78-130">-Name</span></span>
<span data-ttu-id="9ec78-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9ec78-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="9ec78-132">-NetworkSetting</span></span>
<span data-ttu-id="9ec78-133">Obtém as configurações de rede do dispositivo de gateway de caixa de dados de borda/caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="9ec78-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec78-134">-ResourceGroupName</span></span>
<span data-ttu-id="9ec78-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9ec78-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec78-136">-ResourceId</span></span>
<span data-ttu-id="9ec78-137">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="9ec78-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="9ec78-138">-UpdateSummary</span></span>
<span data-ttu-id="9ec78-139">Obtém informações sobre a disponibilidade de atualizações com base na última verificação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ec78-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="9ec78-140">Ele também obtém informações sobre qualquer trabalho de download ou de instalação em andamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ec78-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec78-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec78-141">CommonParameters</span></span>
<span data-ttu-id="9ec78-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec78-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec78-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ec78-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec78-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ec78-144">INPUTS</span></span>

### <span data-ttu-id="9ec78-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9ec78-145">None</span></span>

## <span data-ttu-id="9ec78-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ec78-146">OUTPUTS</span></span>

### <span data-ttu-id="9ec78-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9ec78-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="9ec78-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="9ec78-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="9ec78-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="9ec78-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="9ec78-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="9ec78-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="9ec78-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="9ec78-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="9ec78-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ec78-152">NOTES</span></span>

## <span data-ttu-id="9ec78-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ec78-153">RELATED LINKS</span></span>
