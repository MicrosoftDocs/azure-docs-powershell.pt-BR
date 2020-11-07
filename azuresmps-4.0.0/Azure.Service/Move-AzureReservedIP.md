---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946242"
---
# <span data-ttu-id="c60c5-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c60c5-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="c60c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c60c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c60c5-103">Migra um endereço IP reservado para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c60c5-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c60c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c60c5-104">SYNTAX</span></span>

### <span data-ttu-id="c60c5-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60c5-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c60c5-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60c5-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c60c5-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60c5-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c60c5-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60c5-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c60c5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c60c5-109">DESCRIPTION</span></span>
<span data-ttu-id="c60c5-110">O cmdlet **move-AzureReservedIP** migra um endereço IP reservado para um grupo de recursos na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c60c5-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c60c5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c60c5-111">EXAMPLES</span></span>

### <span data-ttu-id="c60c5-112">1:</span><span class="sxs-lookup"><span data-stu-id="c60c5-112">1:</span></span>
```

```

## <span data-ttu-id="c60c5-113">OS</span><span class="sxs-lookup"><span data-stu-id="c60c5-113">PARAMETERS</span></span>

### <span data-ttu-id="c60c5-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="c60c5-114">-Abort</span></span>
<span data-ttu-id="c60c5-115">Indica que esse cmdlet cancela a migração de endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="c60c5-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

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

### <span data-ttu-id="c60c5-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c60c5-116">-Commit</span></span>
<span data-ttu-id="c60c5-117">Indica que esse cmdlet inicia a migração de endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="c60c5-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

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

### <span data-ttu-id="c60c5-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c60c5-118">-InformationAction</span></span>
<span data-ttu-id="c60c5-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="c60c5-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c60c5-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c60c5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c60c5-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="c60c5-121">Continue</span></span>
- <span data-ttu-id="c60c5-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c60c5-122">Ignore</span></span>
- <span data-ttu-id="c60c5-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="c60c5-123">Inquire</span></span>
- <span data-ttu-id="c60c5-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c60c5-124">SilentlyContinue</span></span>
- <span data-ttu-id="c60c5-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="c60c5-125">Stop</span></span>
- <span data-ttu-id="c60c5-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="c60c5-126">Suspend</span></span>

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

### <span data-ttu-id="c60c5-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c60c5-127">-InformationVariable</span></span>
<span data-ttu-id="c60c5-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="c60c5-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c60c5-129">-Prepare</span><span class="sxs-lookup"><span data-stu-id="c60c5-129">-Prepare</span></span>
<span data-ttu-id="c60c5-130">Indica que esse cmdlet prepara o endereço IP reservado para migração.</span><span class="sxs-lookup"><span data-stu-id="c60c5-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="c60c5-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c60c5-131">-Profile</span></span>
<span data-ttu-id="c60c5-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c60c5-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c60c5-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c60c5-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c60c5-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="c60c5-134">-ReservedIPName</span></span>
<span data-ttu-id="c60c5-135">Especifica o nome do endereço IP reservado que este cmdlet migra.</span><span class="sxs-lookup"><span data-stu-id="c60c5-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="c60c5-136">-Validar</span><span class="sxs-lookup"><span data-stu-id="c60c5-136">-Validate</span></span>
<span data-ttu-id="c60c5-137">Especifica que esse cmdlet valide o endereço IP reservado para migração.</span><span class="sxs-lookup"><span data-stu-id="c60c5-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="c60c5-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c60c5-138">-Confirm</span></span>
<span data-ttu-id="c60c5-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c60c5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60c5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c60c5-140">-WhatIf</span></span>
<span data-ttu-id="c60c5-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c60c5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c60c5-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c60c5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60c5-143">CommonParameters</span></span>
<span data-ttu-id="c60c5-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60c5-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c60c5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60c5-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c60c5-146">INPUTS</span></span>

## <span data-ttu-id="c60c5-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c60c5-147">OUTPUTS</span></span>

## <span data-ttu-id="c60c5-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c60c5-148">NOTES</span></span>

## <span data-ttu-id="c60c5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c60c5-149">RELATED LINKS</span></span>

[<span data-ttu-id="c60c5-150">Mover-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c60c5-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="c60c5-151">Mover-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c60c5-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="c60c5-152">Mover-AzureService</span><span class="sxs-lookup"><span data-stu-id="c60c5-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="c60c5-153">Mover-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c60c5-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="c60c5-154">Mover-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c60c5-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


