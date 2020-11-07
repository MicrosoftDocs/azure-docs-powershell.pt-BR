---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945590"
---
# <span data-ttu-id="e4bbd-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e4bbd-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="e4bbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bbd-103">Obtém mapeamentos de rede para um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="e4bbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4bbd-104">SYNTAX</span></span>

### <span data-ttu-id="e4bbd-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e4bbd-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e4bbd-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="e4bbd-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4bbd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="e4bbd-108">O cmdlet **Get-AzureSiteRecoveryNetworkMapping** Obtém informações sobre os mapeamentos de rede do Azure site Recovery para o cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="e4bbd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="e4bbd-110">Exemplo 1: obter o mapeamento entre uma rede e uma rede de recuperação</span><span class="sxs-lookup"><span data-stu-id="e4bbd-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="e4bbd-111">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="e4bbd-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="e4bbd-112">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="e4bbd-113">O segundo comando obtém o mapeamento entre a rede principal e a rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="e4bbd-114">O comando especifica o servidor primário para o mapeamento de rede como o primeiro elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="e4bbd-115">O comando especifica o servidor para a rede de recuperação como o segundo elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="e4bbd-116">Exemplo 2: obter o mapeamento entre uma rede e uma rede de máquina virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="e4bbd-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="e4bbd-117">O primeiro cmdlet de comando obtém servidores para o cofre de recuperação de site atual.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="e4bbd-118">O comando armazena os servidores na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="e4bbd-119">O segundo comando obtém um mapeamento entre a rede principal e uma rede de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="e4bbd-120">O comando especifica o servidor primário da rede como o primeiro elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="e4bbd-121">O comando especifica o parâmetro *do Azure* .</span><span class="sxs-lookup"><span data-stu-id="e4bbd-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="e4bbd-122">Portanto, o comando obtém o mapeamento para uma rede de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="e4bbd-123">OS</span><span class="sxs-lookup"><span data-stu-id="e4bbd-123">PARAMETERS</span></span>

### <span data-ttu-id="e4bbd-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="e4bbd-124">-Azure</span></span>
<span data-ttu-id="e4bbd-125">Indica que esse cmdlet obtém mapeamentos de rede para redes no servidor primário mapeado para redes virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bbd-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="e4bbd-126">-PrimaryServer</span></span>
<span data-ttu-id="e4bbd-127">Especifica um servidor primário para o qual obter mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bbd-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e4bbd-128">-Profile</span></span>
<span data-ttu-id="e4bbd-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4bbd-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bbd-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e4bbd-131">-RecoveryServer</span></span>
<span data-ttu-id="e4bbd-132">Especifica um servidor de recuperação para o qual obter mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bbd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bbd-133">CommonParameters</span></span>
<span data-ttu-id="e4bbd-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bbd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bbd-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bbd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bbd-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4bbd-136">INPUTS</span></span>

## <span data-ttu-id="e4bbd-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4bbd-137">OUTPUTS</span></span>

## <span data-ttu-id="e4bbd-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4bbd-138">NOTES</span></span>

## <span data-ttu-id="e4bbd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4bbd-139">RELATED LINKS</span></span>

[<span data-ttu-id="e4bbd-140">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e4bbd-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="e4bbd-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e4bbd-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


