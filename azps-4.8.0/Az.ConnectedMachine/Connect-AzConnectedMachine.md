---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955718"
---
# <span data-ttu-id="c9829-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="c9829-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="c9829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9829-102">SYNOPSIS</span></span>
<span data-ttu-id="c9829-103">API para registrar um novo computador e, assim, criar um recurso controlado no ARM</span><span class="sxs-lookup"><span data-stu-id="c9829-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c9829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9829-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="c9829-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9829-105">DESCRIPTION</span></span>
<span data-ttu-id="c9829-106">API para registrar um novo computador e, assim, criar um recurso controlado no ARM</span><span class="sxs-lookup"><span data-stu-id="c9829-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c9829-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9829-107">EXAMPLES</span></span>

### <span data-ttu-id="c9829-108">Exemplo 1: embuti o computador em que você está conectado como um computador conectado</span><span class="sxs-lookup"><span data-stu-id="c9829-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="c9829-109">O computador em que você está conectado como um computador conectado.</span><span class="sxs-lookup"><span data-stu-id="c9829-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="c9829-110">Exemplo 2: embuti um computador remoto como um dispositivo conectado</span><span class="sxs-lookup"><span data-stu-id="c9829-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="c9829-111">O integrada a um computador remoto como um dispositivo conectado usando a comunicação remota do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9829-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="c9829-112">Observação: somente o Windows como destino tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="c9829-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="c9829-113">OS</span><span class="sxs-lookup"><span data-stu-id="c9829-113">PARAMETERS</span></span>

### <span data-ttu-id="c9829-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9829-114">-DefaultProfile</span></span>
<span data-ttu-id="c9829-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9829-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9829-116">-Local</span><span class="sxs-lookup"><span data-stu-id="c9829-116">-Location</span></span>
<span data-ttu-id="c9829-117">O local do ConnectedMachine criado.</span><span class="sxs-lookup"><span data-stu-id="c9829-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="c9829-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9829-118">-Name</span></span>
<span data-ttu-id="c9829-119">O nome que será usado para esta máquina.</span><span class="sxs-lookup"><span data-stu-id="c9829-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="c9829-120">O nome do host é usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="c9829-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="c9829-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="c9829-121">-Proxy</span></span>
<span data-ttu-id="c9829-122">O URI do servidor proxy a ser usado</span><span class="sxs-lookup"><span data-stu-id="c9829-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="c9829-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="c9829-123">-PSSession</span></span>
<span data-ttu-id="c9829-124">Quando especificado, o comando que os computadores que se encontram na máquina do Azure para o Azure serão executados em cada PSSession.</span><span class="sxs-lookup"><span data-stu-id="c9829-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="c9829-125">Observação: isso só funciona no Windows por enquanto.</span><span class="sxs-lookup"><span data-stu-id="c9829-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="c9829-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9829-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9829-127">O nome do grupo de recursos ao qual você deseja adicionar a máquina.</span><span class="sxs-lookup"><span data-stu-id="c9829-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="c9829-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9829-128">-SubscriptionId</span></span>
<span data-ttu-id="c9829-129">A ID da assinatura à qual você deseja adicionar a máquina.</span><span class="sxs-lookup"><span data-stu-id="c9829-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="c9829-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="c9829-130">-Tag</span></span>
<span data-ttu-id="c9829-131">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c9829-131">Resource tags.</span></span>

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

### <span data-ttu-id="c9829-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9829-132">CommonParameters</span></span>
<span data-ttu-id="c9829-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9829-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9829-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9829-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9829-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9829-135">INPUTS</span></span>

## <span data-ttu-id="c9829-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9829-136">OUTPUTS</span></span>

## <span data-ttu-id="c9829-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9829-137">NOTES</span></span>

<span data-ttu-id="c9829-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c9829-138">ALIASES</span></span>

## <span data-ttu-id="c9829-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9829-139">RELATED LINKS</span></span>

