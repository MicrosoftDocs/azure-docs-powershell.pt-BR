---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946110"
---
# <span data-ttu-id="f404d-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f404d-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="f404d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f404d-102">SYNOPSIS</span></span>
<span data-ttu-id="f404d-103">Remove um mapeamento de rede de um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="f404d-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="f404d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f404d-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f404d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f404d-105">DESCRIPTION</span></span>
<span data-ttu-id="f404d-106">O cmdlet **Remove-AzureSiteRecoveryNetworkMapping** remove um mapeamento de rede do cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="f404d-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f404d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f404d-107">EXAMPLES</span></span>

### <span data-ttu-id="f404d-108">Exemplo 1: remover o mapeamento entre uma rede e uma rede de recuperação</span><span class="sxs-lookup"><span data-stu-id="f404d-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="f404d-109">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="f404d-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="f404d-110">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="f404d-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f404d-111">O segundo comando obtém o mapeamento entre a rede principal e a rede de recuperação e, em seguida, armazena-a na variável $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f404d-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="f404d-112">O comando especifica o servidor primário para o mapeamento de rede como o primeiro elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="f404d-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="f404d-113">O comando especifica o servidor para a rede de recuperação como o segundo elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="f404d-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="f404d-114">O comando final remove o mapeamento de rede em $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f404d-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="f404d-115">Exemplo 2: remover o mapeamento entre uma rede e uma rede de máquina virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="f404d-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="f404d-116">O primeiro cmdlet de comando obtém servidores para o cofre de recuperação de site atual.</span><span class="sxs-lookup"><span data-stu-id="f404d-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="f404d-117">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="f404d-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f404d-118">O segundo comando obtém um mapeamento entre a rede principal e uma rede de máquina virtual do Azure e, em seguida, armazena-a na variável $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f404d-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="f404d-119">O comando especifica o servidor primário da rede como o primeiro elemento de $Servers.</span><span class="sxs-lookup"><span data-stu-id="f404d-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="f404d-120">O comando especifica o parâmetro *do Azure* .</span><span class="sxs-lookup"><span data-stu-id="f404d-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="f404d-121">Portanto, o comando obtém o mapeamento para uma rede de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f404d-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="f404d-122">O comando final remove o mapeamento de rede em $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f404d-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="f404d-123">OS</span><span class="sxs-lookup"><span data-stu-id="f404d-123">PARAMETERS</span></span>

### <span data-ttu-id="f404d-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f404d-124">-NetworkMapping</span></span>
<span data-ttu-id="f404d-125">Especifica o mapeamento de rede a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f404d-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f404d-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f404d-126">-Profile</span></span>
<span data-ttu-id="f404d-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f404d-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f404d-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f404d-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f404d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f404d-129">CommonParameters</span></span>
<span data-ttu-id="f404d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f404d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f404d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f404d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f404d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f404d-132">INPUTS</span></span>

## <span data-ttu-id="f404d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f404d-133">OUTPUTS</span></span>

## <span data-ttu-id="f404d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f404d-134">NOTES</span></span>

## <span data-ttu-id="f404d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f404d-135">RELATED LINKS</span></span>

[<span data-ttu-id="f404d-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f404d-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="f404d-137">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f404d-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="f404d-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="f404d-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


