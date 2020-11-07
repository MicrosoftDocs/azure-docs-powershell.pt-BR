---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946015"
---
# <span data-ttu-id="850fe-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="850fe-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="850fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="850fe-102">SYNOPSIS</span></span>
<span data-ttu-id="850fe-103">Atualiza as propriedades de uma entidade de proteção no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="850fe-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="850fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="850fe-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="850fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="850fe-105">DESCRIPTION</span></span>
<span data-ttu-id="850fe-106">O cmdlet **Update-AzureSiteRecoveryProtectionEntity** atualiza as propriedades de uma entidade de proteção no Azure site Recovery, como informações de proprietário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="850fe-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="850fe-107">Esse cmdlet tem suporte apenas para o VMM (Virtual Machine monitor) para entidades de proteção protegida do VMM.</span><span class="sxs-lookup"><span data-stu-id="850fe-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="850fe-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="850fe-108">EXAMPLES</span></span>

### <span data-ttu-id="850fe-109">Exemplo 1: atualizar uma entidade de proteção</span><span class="sxs-lookup"><span data-stu-id="850fe-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="850fe-110">O primeiro comando obtém um contêiner protegido usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e armazena esse objeto na variável $container.</span><span class="sxs-lookup"><span data-stu-id="850fe-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="850fe-111">O segundo comando obtém a máquina virtual protegida que pertence ao contêiner armazenado no $Container usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** e, em seguida, armazena-o na variável $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="850fe-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="850fe-112">O comando final atualiza a entidade de proteção em $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="850fe-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="850fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="850fe-113">PARAMETERS</span></span>

### <span data-ttu-id="850fe-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="850fe-114">-Profile</span></span>
<span data-ttu-id="850fe-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="850fe-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="850fe-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="850fe-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="850fe-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="850fe-117">-ProtectionEntity</span></span>
<span data-ttu-id="850fe-118">Especifica uma entidade de proteção a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="850fe-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="850fe-119">Para obter um objeto **ASRProtectionEntity** , use o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="850fe-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="850fe-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="850fe-120">-WaitForCompletion</span></span>
<span data-ttu-id="850fe-121">Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="850fe-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850fe-122">CommonParameters</span></span>
<span data-ttu-id="850fe-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="850fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850fe-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="850fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850fe-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="850fe-125">INPUTS</span></span>

## <span data-ttu-id="850fe-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="850fe-126">OUTPUTS</span></span>

## <span data-ttu-id="850fe-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="850fe-127">NOTES</span></span>

## <span data-ttu-id="850fe-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="850fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="850fe-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="850fe-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="850fe-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="850fe-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="850fe-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="850fe-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


