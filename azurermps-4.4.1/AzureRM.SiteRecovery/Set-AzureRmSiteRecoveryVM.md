---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 7cfc764e5c9c3c5bb11290220cc04b2baa781070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432538"
---
# <span data-ttu-id="c44d8-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="c44d8-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="c44d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c44d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c44d8-103">Define as opções do lado de recuperação de uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c44d8-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c44d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c44d8-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c44d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c44d8-105">DESCRIPTION</span></span>
<span data-ttu-id="c44d8-106">O cmdlet **set-AzureRmSiteRecoveryVM** define as opções de proteção do lado de recuperação, como o tamanho da máquina virtual de recuperação e a rede de máquina virtual de recuperação, para entidades de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c44d8-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="c44d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c44d8-107">EXAMPLES</span></span>

## <span data-ttu-id="c44d8-108">OS</span><span class="sxs-lookup"><span data-stu-id="c44d8-108">PARAMETERS</span></span>

### <span data-ttu-id="c44d8-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="c44d8-109">-Name</span></span>
<span data-ttu-id="c44d8-110">Especifica o nome da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="c44d8-110">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-111">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="c44d8-111">-NicSelectionType</span></span>
<span data-ttu-id="c44d8-112">Especifica as propriedades de seleção do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="c44d8-112">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="c44d8-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c44d8-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c44d8-114">Não selecionado</span><span class="sxs-lookup"><span data-stu-id="c44d8-114">NotSelected</span></span>
- <span data-ttu-id="c44d8-115">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="c44d8-115">SelectedByUser</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="c44d8-116">-PrimaryNic</span></span>
<span data-ttu-id="c44d8-117">Especifica a placa adaptadora de rede principal.</span><span class="sxs-lookup"><span data-stu-id="c44d8-117">Specifies the primary network adapter card.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="c44d8-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="c44d8-119">Especifica a ID de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c44d8-119">Specifies the recovery network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="c44d8-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="c44d8-121">Especifica o endereço IP estático atribuído ao controlador de adaptador de rede primário na recuperação.</span><span class="sxs-lookup"><span data-stu-id="c44d8-121">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c44d8-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="c44d8-123">Especifica o nome de sub-rede da rede virtual do Azure com a qual anexar o controlador de adaptador de rede primário na recuperação.</span><span class="sxs-lookup"><span data-stu-id="c44d8-123">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-124">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="c44d8-124">-Size</span></span>
<span data-ttu-id="c44d8-125">Especifica o tamanho da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="c44d8-125">Specifies the target virtual machine size.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-126">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c44d8-126">-VirtualMachine</span></span>
<span data-ttu-id="c44d8-127">Especifica o objeto da máquina virtual de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="c44d8-127">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44d8-128">-DefaultProfile</span></span>
<span data-ttu-id="c44d8-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c44d8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44d8-130">CommonParameters</span></span>
<span data-ttu-id="c44d8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44d8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44d8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44d8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c44d8-133">INPUTS</span></span>

### <span data-ttu-id="c44d8-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c44d8-134">ASRVirtualMachine</span></span>
<span data-ttu-id="c44d8-135">O parâmetro ' VirtualMachine ' aceita o valor do tipo ' ASRVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c44d8-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="c44d8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c44d8-136">OUTPUTS</span></span>

### <span data-ttu-id="c44d8-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c44d8-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c44d8-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c44d8-138">NOTES</span></span>

## <span data-ttu-id="c44d8-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c44d8-139">RELATED LINKS</span></span>

[<span data-ttu-id="c44d8-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="c44d8-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
