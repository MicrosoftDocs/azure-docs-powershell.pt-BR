---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433040"
---
# <span data-ttu-id="32dc2-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="32dc2-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="32dc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="32dc2-103">Cria um mapeamento de rede ASR entre duas redes.</span><span class="sxs-lookup"><span data-stu-id="32dc2-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32dc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32dc2-104">SYNTAX</span></span>

### <span data-ttu-id="32dc2-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="32dc2-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32dc2-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="32dc2-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32dc2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="32dc2-108">O cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** inicia a operação de criação de um mapeamento de rede ASR entre duas redes e retorna o objeto de trabalho ASR para o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="32dc2-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="32dc2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="32dc2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32dc2-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="32dc2-111">Inicia a operação de criação de mapeamento de rede usando o nome, as redes primárias e de recuperação especificadas e retorna um trabalho ASR para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="32dc2-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="32dc2-112">OS</span><span class="sxs-lookup"><span data-stu-id="32dc2-112">PARAMETERS</span></span>

### <span data-ttu-id="32dc2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="32dc2-113">-Name</span></span>
<span data-ttu-id="32dc2-114">Nome do mapeamento de rede ASR a ser criado.</span><span class="sxs-lookup"><span data-stu-id="32dc2-114">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32dc2-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="32dc2-115">-PrimaryNetwork</span></span>
<span data-ttu-id="32dc2-116">Especifica o objeto de rede principal para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="32dc2-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32dc2-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="32dc2-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="32dc2-118">Especifica a ID de rede de recuperação do Azure para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="32dc2-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="32dc2-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="32dc2-119">-RecoveryNetwork</span></span>
<span data-ttu-id="32dc2-120">Especifica o objeto de rede de recuperação para o mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="32dc2-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="32dc2-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32dc2-121">-Confirm</span></span>
<span data-ttu-id="32dc2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32dc2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32dc2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32dc2-123">-WhatIf</span></span>
<span data-ttu-id="32dc2-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32dc2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32dc2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32dc2-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32dc2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32dc2-126">CommonParameters</span></span>
<span data-ttu-id="32dc2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32dc2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32dc2-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32dc2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32dc2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32dc2-129">INPUTS</span></span>

### <span data-ttu-id="32dc2-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="32dc2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="32dc2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32dc2-131">OUTPUTS</span></span>

### <span data-ttu-id="32dc2-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="32dc2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="32dc2-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32dc2-133">NOTES</span></span>

## <span data-ttu-id="32dc2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32dc2-134">RELATED LINKS</span></span>

[<span data-ttu-id="32dc2-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="32dc2-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="32dc2-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="32dc2-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
