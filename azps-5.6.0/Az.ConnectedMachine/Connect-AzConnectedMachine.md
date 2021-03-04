---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: b0e52f6d163579e1d481f841d3a58e8b15c6658b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893205"
---
# <span data-ttu-id="95efa-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="95efa-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="95efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95efa-102">SYNOPSIS</span></span>
<span data-ttu-id="95efa-103">API para registrar um novo computador e, assim, criar um recurso rastreado no ARM</span><span class="sxs-lookup"><span data-stu-id="95efa-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="95efa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95efa-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="95efa-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95efa-105">DESCRIPTION</span></span>
<span data-ttu-id="95efa-106">API para registrar um novo computador e, assim, criar um recurso rastreado no ARM</span><span class="sxs-lookup"><span data-stu-id="95efa-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="95efa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95efa-107">EXAMPLES</span></span>

### <span data-ttu-id="95efa-108">Exemplo 1: integra o computador em que você está como um computador conectado</span><span class="sxs-lookup"><span data-stu-id="95efa-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="95efa-109">Integra o computador em que você está como uma máquina conectada.</span><span class="sxs-lookup"><span data-stu-id="95efa-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="95efa-110">Exemplo 2: Integra uma máquina remota como um dispositivo conectado</span><span class="sxs-lookup"><span data-stu-id="95efa-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="95efa-111">Integra uma máquina remota como um dispositivo conectado usando a remoção do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95efa-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="95efa-112">Observação: somente o Windows como destino é suportado no momento.</span><span class="sxs-lookup"><span data-stu-id="95efa-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="95efa-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95efa-113">PARAMETERS</span></span>

### <span data-ttu-id="95efa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95efa-114">-DefaultProfile</span></span>
<span data-ttu-id="95efa-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95efa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-116">-Location</span><span class="sxs-lookup"><span data-stu-id="95efa-116">-Location</span></span>
<span data-ttu-id="95efa-117">O local do ConnectedMachine criado.</span><span class="sxs-lookup"><span data-stu-id="95efa-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="95efa-118">-Name</span></span>
<span data-ttu-id="95efa-119">O nome que será usado para este computador.</span><span class="sxs-lookup"><span data-stu-id="95efa-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="95efa-120">O nome do host é usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="95efa-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="95efa-121">-Proxy</span></span>
<span data-ttu-id="95efa-122">O URI do servidor proxy a ser usado</span><span class="sxs-lookup"><span data-stu-id="95efa-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="95efa-123">-PSSession</span></span>
<span data-ttu-id="95efa-124">Quando especificado, o comando que integra máquinas ao Azure será executado em cada PSSession.</span><span class="sxs-lookup"><span data-stu-id="95efa-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="95efa-125">OBSERVAÇÃO: Isso só funciona no Windows por enquanto.</span><span class="sxs-lookup"><span data-stu-id="95efa-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95efa-126">-ResourceGroupName</span></span>
<span data-ttu-id="95efa-127">O nome do grupo de recursos ao que você deseja adicionar o computador.</span><span class="sxs-lookup"><span data-stu-id="95efa-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95efa-128">-SubscriptionId</span></span>
<span data-ttu-id="95efa-129">A ID da assinatura à que você deseja adicionar o computador.</span><span class="sxs-lookup"><span data-stu-id="95efa-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="95efa-130">-Tag</span></span>
<span data-ttu-id="95efa-131">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="95efa-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95efa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95efa-132">CommonParameters</span></span>
<span data-ttu-id="95efa-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95efa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95efa-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95efa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95efa-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95efa-135">INPUTS</span></span>

## <span data-ttu-id="95efa-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95efa-136">OUTPUTS</span></span>

## <span data-ttu-id="95efa-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="95efa-137">NOTES</span></span>

<span data-ttu-id="95efa-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="95efa-138">ALIASES</span></span>

## <span data-ttu-id="95efa-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95efa-139">RELATED LINKS</span></span>

