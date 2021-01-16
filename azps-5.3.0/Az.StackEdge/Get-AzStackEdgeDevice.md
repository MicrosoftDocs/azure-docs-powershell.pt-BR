---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: 1fa868d9df41a5f4f995981c332497d9555e1174
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433802"
---
# <span data-ttu-id="c6f7f-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c6f7f-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c6f7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f7f-103">Obtém as informações sobre dispositivos de borda de pilha disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="c6f7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6f7f-104">SYNTAX</span></span>

### <span data-ttu-id="c6f7f-105">ListByParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6f7f-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f7f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6f7f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f7f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6f7f-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f7f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6f7f-108">DESCRIPTION</span></span>
<span data-ttu-id="c6f7f-109">O cmdlet **Get-AzStackEdgeDevice** Obtém as informações sobre os dispositivos de borda de pilha disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="c6f7f-110">Você pode especificar o nome do dispositivo juntamente com o nome do grupo de recursos para obter as informações em um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="c6f7f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6f7f-111">EXAMPLES</span></span>

### <span data-ttu-id="c6f7f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6f7f-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="c6f7f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6f7f-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="c6f7f-114">OS</span><span class="sxs-lookup"><span data-stu-id="c6f7f-114">PARAMETERS</span></span>

### <span data-ttu-id="c6f7f-115">-Alerta</span><span class="sxs-lookup"><span data-stu-id="c6f7f-115">-Alert</span></span>
<span data-ttu-id="c6f7f-116">Buscar os alertas no dispositivo de borda/gateway de pilha</span><span class="sxs-lookup"><span data-stu-id="c6f7f-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f7f-117">-DefaultProfile</span></span>
<span data-ttu-id="c6f7f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f7f-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="c6f7f-119">-ExtendedInfo</span></span>
<span data-ttu-id="c6f7f-120">Obtém informações adicionais para o dispositivo de gateway Edge/Stack de pilha especificado</span><span class="sxs-lookup"><span data-stu-id="c6f7f-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6f7f-121">-Name</span></span>
<span data-ttu-id="c6f7f-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c6f7f-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="c6f7f-123">-NetworkSetting</span></span>
<span data-ttu-id="c6f7f-124">Obtém as configurações de rede do dispositivo de gateway de pilha/pilha especificado da pilha</span><span class="sxs-lookup"><span data-stu-id="c6f7f-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f7f-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6f7f-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c6f7f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6f7f-127">-ResourceId</span></span>
<span data-ttu-id="c6f7f-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="c6f7f-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="c6f7f-129">-UpdateSummary</span></span>
<span data-ttu-id="c6f7f-130">Obtém informações sobre a disponibilidade de atualizações com base na última verificação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="c6f7f-131">Ele também obtém informações sobre qualquer trabalho de download ou de instalação em andamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f7f-132">CommonParameters</span></span>
<span data-ttu-id="c6f7f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f7f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6f7f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f7f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6f7f-135">INPUTS</span></span>

## <span data-ttu-id="c6f7f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6f7f-136">OUTPUTS</span></span>

## <span data-ttu-id="c6f7f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6f7f-137">NOTES</span></span>

## <span data-ttu-id="c6f7f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6f7f-138">RELATED LINKS</span></span>
