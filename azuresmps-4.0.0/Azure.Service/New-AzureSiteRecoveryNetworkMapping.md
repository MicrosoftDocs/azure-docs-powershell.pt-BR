---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946217"
---
# <span data-ttu-id="c7ad1-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7ad1-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="c7ad1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ad1-103">Cria um mapeamento entre redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="c7ad1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7ad1-104">SYNTAX</span></span>

### <span data-ttu-id="c7ad1-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c7ad1-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7ad1-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c7ad1-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7ad1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7ad1-107">DESCRIPTION</span></span>
<span data-ttu-id="c7ad1-108">O cmdlet **New-AzureSiteRecoveryNetworkMapping** cria um mapeamento entre duas redes virtuais e retorna um trabalho do Azure site Recovery para controlá-la.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="c7ad1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7ad1-109">EXAMPLES</span></span>

### <span data-ttu-id="c7ad1-110">Exemplo 1: criar um mapeamento entre uma rede e uma rede de recuperação</span><span class="sxs-lookup"><span data-stu-id="c7ad1-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="c7ad1-111">O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="c7ad1-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="c7ad1-112">O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="c7ad1-113">O segundo comando obtém a rede de recuperação de site para o primeiro servidor na matriz $Servers usando o cmdlet **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="c7ad1-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="c7ad1-114">O comando armazena as redes na variável $Networks.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="c7ad1-115">O comando final cria um mapeamento entre a rede principal e a rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="c7ad1-116">O comando especifica a rede principal como o primeiro elemento de $Networks.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="c7ad1-117">O comando especifica a rede de recuperação como o segundo elemento de $Networks.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="c7ad1-118">OS</span><span class="sxs-lookup"><span data-stu-id="c7ad1-118">PARAMETERS</span></span>

### <span data-ttu-id="c7ad1-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7ad1-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="c7ad1-120">Especifica a ID da sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad1-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c7ad1-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="c7ad1-122">Especifica a ID de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad1-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c7ad1-123">-PrimaryNetwork</span></span>
<span data-ttu-id="c7ad1-124">Especifica o objeto de rede principal.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad1-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c7ad1-125">-Profile</span></span>
<span data-ttu-id="c7ad1-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7ad1-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7ad1-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c7ad1-128">-RecoveryNetwork</span></span>
<span data-ttu-id="c7ad1-129">Especifica o objeto de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ad1-130">CommonParameters</span></span>
<span data-ttu-id="c7ad1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7ad1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ad1-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ad1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ad1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7ad1-133">INPUTS</span></span>

## <span data-ttu-id="c7ad1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7ad1-134">OUTPUTS</span></span>

## <span data-ttu-id="c7ad1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7ad1-135">NOTES</span></span>

## <span data-ttu-id="c7ad1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7ad1-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7ad1-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7ad1-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="c7ad1-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c7ad1-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="c7ad1-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7ad1-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


