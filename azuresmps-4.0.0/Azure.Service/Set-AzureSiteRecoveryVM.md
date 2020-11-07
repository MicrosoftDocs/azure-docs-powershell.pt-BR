---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945754"
---
# <span data-ttu-id="76155-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="76155-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="76155-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76155-102">SYNOPSIS</span></span>
<span data-ttu-id="76155-103">Define as opções do lado de recuperação de uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="76155-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="76155-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76155-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="76155-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76155-105">DESCRIPTION</span></span>
<span data-ttu-id="76155-106">O cmdlet **set-AzureSiteRecoveryVM** define as opções de proteção do lado de recuperação, como o tamanho da máquina virtual de recuperação e a rede de máquina virtual de recuperação, para entidades de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="76155-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="76155-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76155-107">EXAMPLES</span></span>

### <span data-ttu-id="76155-108">Exemplo 1: permitir a atualização em uma máquina virtual protegida</span><span class="sxs-lookup"><span data-stu-id="76155-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="76155-109">O primeiro comando usa o cmdlet **Get-AzureSiteRecoveryProtectionContainer** para obter um contêiner protegido e, em seguida, armazena-o na variável $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="76155-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="76155-110">O segundo comando obtém as máquinas virtuais no $ProtectionContainer usando o cmdlet **Get-AzureSiteRecoveryVM** e, em seguida, armazena-os na variável $VitrualMachines.</span><span class="sxs-lookup"><span data-stu-id="76155-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="76155-111">O comando final permite atualizações para a primeira máquina virtual na matriz $VitrualMachines, chamada NewVirtualMachine05.</span><span class="sxs-lookup"><span data-stu-id="76155-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="76155-112">OS</span><span class="sxs-lookup"><span data-stu-id="76155-112">PARAMETERS</span></span>

### <span data-ttu-id="76155-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="76155-113">-Name</span></span>
<span data-ttu-id="76155-114">Especifica o nome da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="76155-114">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="76155-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="76155-115">-PrimaryNic</span></span>
<span data-ttu-id="76155-116">Especifica a placa adaptadora de rede principal.</span><span class="sxs-lookup"><span data-stu-id="76155-116">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="76155-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="76155-117">-Profile</span></span>
<span data-ttu-id="76155-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="76155-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76155-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="76155-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76155-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="76155-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="76155-121">Especifica a ID de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="76155-121">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="76155-122">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="76155-122">-Size</span></span>
<span data-ttu-id="76155-123">Especifica o tamanho da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="76155-123">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="76155-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="76155-124">-VirtualMachine</span></span>
<span data-ttu-id="76155-125">Especifica o objeto da máquina virtual de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="76155-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76155-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76155-126">CommonParameters</span></span>
<span data-ttu-id="76155-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76155-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76155-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76155-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76155-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76155-129">INPUTS</span></span>

## <span data-ttu-id="76155-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76155-130">OUTPUTS</span></span>

## <span data-ttu-id="76155-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76155-131">NOTES</span></span>

## <span data-ttu-id="76155-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76155-132">RELATED LINKS</span></span>

[<span data-ttu-id="76155-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="76155-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="76155-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="76155-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


