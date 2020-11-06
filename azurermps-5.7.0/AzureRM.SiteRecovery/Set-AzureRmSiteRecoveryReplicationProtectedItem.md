---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e09cc216b7ba3ef383467ea53478cfe8819e0a4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433377"
---
# <span data-ttu-id="7bdbf-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdbf-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="7bdbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdbf-103">Define propriedades de recuperação, como a rede de destino e o tamanho da máquina virtual para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bdbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bdbf-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bdbf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bdbf-105">DESCRIPTION</span></span>
<span data-ttu-id="7bdbf-106">O cmdlet **set-AzureRmSiteRecoveryReplicationProtectedItem** define as propriedades de recuperação para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="7bdbf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bdbf-107">EXAMPLES</span></span>

## <span data-ttu-id="7bdbf-108">OS</span><span class="sxs-lookup"><span data-stu-id="7bdbf-108">PARAMETERS</span></span>

### <span data-ttu-id="7bdbf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdbf-109">-DefaultProfile</span></span>
<span data-ttu-id="7bdbf-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-111">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7bdbf-111">-LicenseType</span></span>
<span data-ttu-id="7bdbf-112">Especifica a seleção do tipo de licença para máquinas virtuais do Windows Server migradas por meio do benefício de uso híbrido.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-112">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bdbf-113">-Name</span></span>
<span data-ttu-id="7bdbf-114">Especifica o nome da máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-114">Specifies the name of the recovery virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-115">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="7bdbf-115">-NicSelectionType</span></span>
<span data-ttu-id="7bdbf-116">Especifica as propriedades da NIC (placa de interface de rede) definidas por usuário ou definidas por padrão.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-116">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="7bdbf-117">Você pode especificar não selecionado para voltar aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-117">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="7bdbf-118">-PrimaryNic</span></span>
<span data-ttu-id="7bdbf-119">Especifica a NIC da máquina virtual para a qual esse cmdlet define a propriedade de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-119">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="7bdbf-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="7bdbf-121">Especifica a ID da rede virtual do Azure para a qual esse cmdlet recupera o item protegido.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-121">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="7bdbf-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="7bdbf-123">Especifica o endereço IP estático que deve ser atribuído à NIC primária na recuperação.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-123">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="7bdbf-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="7bdbf-125">Especifica o nome da sub-rede na rede virtual do Azure de recuperação para a qual esse cmdlet recupera o item protegido.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-125">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-126">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdbf-126">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7bdbf-127">Especifica o item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-127">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-128">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="7bdbf-128">-Size</span></span>
<span data-ttu-id="7bdbf-129">Especifica o tamanho da máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-129">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="7bdbf-130">O valor deve ser do conjunto de tamanhos com suporte nas máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-130">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdbf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdbf-131">CommonParameters</span></span>
<span data-ttu-id="7bdbf-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bdbf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdbf-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bdbf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdbf-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bdbf-134">INPUTS</span></span>

### <span data-ttu-id="7bdbf-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdbf-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="7bdbf-136">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7bdbf-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="7bdbf-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bdbf-137">OUTPUTS</span></span>

### <span data-ttu-id="7bdbf-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7bdbf-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7bdbf-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bdbf-139">NOTES</span></span>

## <span data-ttu-id="7bdbf-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bdbf-140">RELATED LINKS</span></span>

[<span data-ttu-id="7bdbf-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdbf-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="7bdbf-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdbf-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="7bdbf-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7bdbf-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
