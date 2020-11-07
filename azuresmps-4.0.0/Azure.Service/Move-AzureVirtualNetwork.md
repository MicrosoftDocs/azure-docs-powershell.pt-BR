---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946238"
---
# <span data-ttu-id="14fd6-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14fd6-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="14fd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="14fd6-103">Migra uma rede virtual para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="14fd6-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="14fd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14fd6-104">SYNTAX</span></span>

### <span data-ttu-id="14fd6-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd6-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14fd6-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd6-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14fd6-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd6-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14fd6-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd6-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14fd6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14fd6-109">DESCRIPTION</span></span>
<span data-ttu-id="14fd6-110">O cmdlet **move-AzureVirtualNetwork** migra uma rede virtual para um grupo de recursos na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="14fd6-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="14fd6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14fd6-111">EXAMPLES</span></span>

### <span data-ttu-id="14fd6-112">Exemplo 1: preparar a migração de rede virtual</span><span class="sxs-lookup"><span data-stu-id="14fd6-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="14fd6-113">Esse comando prepara a rede virtual chamada ContosoVNET para migração para a pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="14fd6-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="14fd6-114">Exemplo 2: iniciar a migração de rede virtual</span><span class="sxs-lookup"><span data-stu-id="14fd6-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="14fd6-115">Esse comando inicia a migração da rede virtual chamada ContosoVNET para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="14fd6-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="14fd6-116">Exemplo 3: validar a migração de rede virtual</span><span class="sxs-lookup"><span data-stu-id="14fd6-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="14fd6-117">Esse comando valida a migração para a rede virtual chamada ContosoVNET para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="14fd6-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="14fd6-118">OS</span><span class="sxs-lookup"><span data-stu-id="14fd6-118">PARAMETERS</span></span>

### <span data-ttu-id="14fd6-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="14fd6-119">-Abort</span></span>
<span data-ttu-id="14fd6-120">Indica que esse cmdlet cancela a migração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="14fd6-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="14fd6-121">-Commit</span></span>
<span data-ttu-id="14fd6-122">Indica que esse cmdlet inicia a migração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="14fd6-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="14fd6-123">-InformationAction</span></span>
<span data-ttu-id="14fd6-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="14fd6-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="14fd6-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="14fd6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="14fd6-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="14fd6-126">Continue</span></span>
- <span data-ttu-id="14fd6-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="14fd6-127">Ignore</span></span>
- <span data-ttu-id="14fd6-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="14fd6-128">Inquire</span></span>
- <span data-ttu-id="14fd6-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14fd6-129">SilentlyContinue</span></span>
- <span data-ttu-id="14fd6-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="14fd6-130">Stop</span></span>
- <span data-ttu-id="14fd6-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="14fd6-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14fd6-132">-InformationVariable</span></span>
<span data-ttu-id="14fd6-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="14fd6-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-134">-Prepare</span><span class="sxs-lookup"><span data-stu-id="14fd6-134">-Prepare</span></span>
<span data-ttu-id="14fd6-135">Indica que esse cmdlet prepara a rede virtual para migração.</span><span class="sxs-lookup"><span data-stu-id="14fd6-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="14fd6-136">-Profile</span></span>
<span data-ttu-id="14fd6-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="14fd6-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14fd6-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="14fd6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14fd6-139">-Validar</span><span class="sxs-lookup"><span data-stu-id="14fd6-139">-Validate</span></span>
<span data-ttu-id="14fd6-140">Especifica que esse cmdlet valida a rede virtual para migração.</span><span class="sxs-lookup"><span data-stu-id="14fd6-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="14fd6-141">-VirtualNetworkName</span></span>
<span data-ttu-id="14fd6-142">Nome da rede virtual a ser migrada</span><span class="sxs-lookup"><span data-stu-id="14fd6-142">Name of the Virtual Network to migrate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14fd6-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14fd6-143">-Confirm</span></span>
<span data-ttu-id="14fd6-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14fd6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14fd6-145">-WhatIf</span></span>
<span data-ttu-id="14fd6-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14fd6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14fd6-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14fd6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14fd6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fd6-148">CommonParameters</span></span>
<span data-ttu-id="14fd6-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14fd6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fd6-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14fd6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fd6-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14fd6-151">INPUTS</span></span>

## <span data-ttu-id="14fd6-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14fd6-152">OUTPUTS</span></span>

## <span data-ttu-id="14fd6-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14fd6-153">NOTES</span></span>

## <span data-ttu-id="14fd6-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14fd6-154">RELATED LINKS</span></span>

[<span data-ttu-id="14fd6-155">Mover-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14fd6-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="14fd6-156">Mover-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="14fd6-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="14fd6-157">Mover-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="14fd6-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="14fd6-158">Mover-AzureService</span><span class="sxs-lookup"><span data-stu-id="14fd6-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="14fd6-159">Mover-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14fd6-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


