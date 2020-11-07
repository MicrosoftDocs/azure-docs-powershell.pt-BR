---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946423"
---
# <span data-ttu-id="d2ed5-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d2ed5-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="d2ed5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ed5-103">Define o estado de uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="d2ed5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2ed5-104">SYNTAX</span></span>

### <span data-ttu-id="d2ed5-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2ed5-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ed5-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="d2ed5-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ed5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2ed5-107">DESCRIPTION</span></span>
<span data-ttu-id="d2ed5-108">O cmdlet **set-AzureSiteRecoveryProtectionEntity** habilita ou desabilita a proteção em uma entidade de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="d2ed5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2ed5-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ed5-110">Exemplo 1: habilitar a proteção para objetos em um contêiner</span><span class="sxs-lookup"><span data-stu-id="d2ed5-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="d2ed5-111">O primeiro comando obtém contêineres para o site atual do Azure site do Azure usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena-o na variável $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="d2ed5-112">O segundo comando obtém as máquinas virtuais protegidas que pertencem ao contêiner armazenado no $ProtectionContainer usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="d2ed5-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="d2ed5-113">O comando armazena os resultados na variável $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="d2ed5-114">O comando final permite proteção para as entidades armazenadas em $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="d2ed5-115">OS</span><span class="sxs-lookup"><span data-stu-id="d2ed5-115">PARAMETERS</span></span>

### <span data-ttu-id="d2ed5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d2ed5-116">-Force</span></span>
<span data-ttu-id="d2ed5-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2ed5-118">-ID</span><span class="sxs-lookup"><span data-stu-id="d2ed5-118">-Id</span></span>
<span data-ttu-id="d2ed5-119">Especifica a ID de uma máquina virtual protegida para a qual habilitar ou desabilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed5-120">-OS</span><span class="sxs-lookup"><span data-stu-id="d2ed5-120">-OS</span></span>
<span data-ttu-id="d2ed5-121">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-121">Specifies the operating system type.</span></span>
<span data-ttu-id="d2ed5-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d2ed5-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2ed5-123">Windows</span><span class="sxs-lookup"><span data-stu-id="d2ed5-123">Windows</span></span>
- <span data-ttu-id="d2ed5-124">Linux</span><span class="sxs-lookup"><span data-stu-id="d2ed5-124">Linux</span></span>

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

### <span data-ttu-id="d2ed5-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="d2ed5-125">-OSDiskName</span></span>
<span data-ttu-id="d2ed5-126">Especifica o nome do disco que contém o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-126">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="d2ed5-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d2ed5-127">-Profile</span></span>
<span data-ttu-id="d2ed5-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2ed5-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2ed5-130">-Proteção</span><span class="sxs-lookup"><span data-stu-id="d2ed5-130">-Protection</span></span>
<span data-ttu-id="d2ed5-131">Especifica se a proteção deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="d2ed5-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d2ed5-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2ed5-133">Ativação</span><span class="sxs-lookup"><span data-stu-id="d2ed5-133">Enable</span></span>
- <span data-ttu-id="d2ed5-134">Desabilita</span><span class="sxs-lookup"><span data-stu-id="d2ed5-134">Disable</span></span>

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

### <span data-ttu-id="d2ed5-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="d2ed5-135">-ProtectionContainerId</span></span>
<span data-ttu-id="d2ed5-136">Especifica a ID de um contêiner protegido.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="d2ed5-137">Este cmdlet habilita ou desabilita a proteção de uma máquina virtual que pertence ao contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed5-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d2ed5-138">-ProtectionEntity</span></span>
<span data-ttu-id="d2ed5-139">Especifica o objeto da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-139">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed5-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="d2ed5-140">-ProtectionProfile</span></span>
<span data-ttu-id="d2ed5-141">Especifica um perfil de proteção para habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="d2ed5-142">Especifique um objeto **ASRProtectionProfile** que seja um dos perfis de proteção disponíveis no contêiner de proteção associado.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed5-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d2ed5-143">-WaitForCompletion</span></span>
<span data-ttu-id="d2ed5-144">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d2ed5-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2ed5-145">-Confirm</span></span>
<span data-ttu-id="d2ed5-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ed5-147">-WhatIf</span></span>
<span data-ttu-id="d2ed5-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ed5-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ed5-150">CommonParameters</span></span>
<span data-ttu-id="d2ed5-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ed5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ed5-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ed5-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ed5-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2ed5-153">INPUTS</span></span>

## <span data-ttu-id="d2ed5-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2ed5-154">OUTPUTS</span></span>

## <span data-ttu-id="d2ed5-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2ed5-155">NOTES</span></span>

## <span data-ttu-id="d2ed5-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2ed5-156">RELATED LINKS</span></span>

[<span data-ttu-id="d2ed5-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d2ed5-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="d2ed5-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d2ed5-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="d2ed5-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d2ed5-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


