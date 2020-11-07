---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946243"
---
# <span data-ttu-id="20063-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20063-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="20063-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20063-102">SYNOPSIS</span></span>
<span data-ttu-id="20063-103">Migra um grupo de segurança de rede para a pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="20063-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="20063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20063-104">SYNTAX</span></span>

### <span data-ttu-id="20063-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="20063-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20063-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="20063-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20063-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="20063-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20063-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="20063-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20063-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20063-109">DESCRIPTION</span></span>
<span data-ttu-id="20063-110">O cmdlet **move-AzureNetworkSecurityGroup** migra um grupo de segurança de rede para um grupo de recursos na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="20063-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="20063-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20063-111">EXAMPLES</span></span>

### <span data-ttu-id="20063-112">1:</span><span class="sxs-lookup"><span data-stu-id="20063-112">1:</span></span>
```

```

## <span data-ttu-id="20063-113">OS</span><span class="sxs-lookup"><span data-stu-id="20063-113">PARAMETERS</span></span>

### <span data-ttu-id="20063-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="20063-114">-Abort</span></span>
<span data-ttu-id="20063-115">Indica que esse cmdlet cancela a migração do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="20063-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="20063-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="20063-116">-Commit</span></span>
<span data-ttu-id="20063-117">Indica que esse cmdlet inicia a migração do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="20063-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="20063-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="20063-118">-InformationAction</span></span>
<span data-ttu-id="20063-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="20063-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20063-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20063-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20063-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="20063-121">Continue</span></span>
- <span data-ttu-id="20063-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="20063-122">Ignore</span></span>
- <span data-ttu-id="20063-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="20063-123">Inquire</span></span>
- <span data-ttu-id="20063-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20063-124">SilentlyContinue</span></span>
- <span data-ttu-id="20063-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="20063-125">Stop</span></span>
- <span data-ttu-id="20063-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="20063-126">Suspend</span></span>

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

### <span data-ttu-id="20063-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20063-127">-InformationVariable</span></span>
<span data-ttu-id="20063-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="20063-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20063-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="20063-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="20063-130">Especifica o nome do grupo de segurança de rede que este cmdlet migra.</span><span class="sxs-lookup"><span data-stu-id="20063-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="20063-131">-Prepare</span><span class="sxs-lookup"><span data-stu-id="20063-131">-Prepare</span></span>
<span data-ttu-id="20063-132">Indica que esse cmdlet prepara o grupo de segurança de rede para migração.</span><span class="sxs-lookup"><span data-stu-id="20063-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="20063-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="20063-133">-Profile</span></span>
<span data-ttu-id="20063-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="20063-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20063-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="20063-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20063-136">-Validar</span><span class="sxs-lookup"><span data-stu-id="20063-136">-Validate</span></span>
<span data-ttu-id="20063-137">Especifica que esse cmdlet valida o grupo de segurança de rede para a migração.</span><span class="sxs-lookup"><span data-stu-id="20063-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="20063-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20063-138">-Confirm</span></span>
<span data-ttu-id="20063-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20063-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20063-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20063-140">-WhatIf</span></span>
<span data-ttu-id="20063-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20063-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20063-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20063-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20063-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20063-143">CommonParameters</span></span>
<span data-ttu-id="20063-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20063-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20063-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20063-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20063-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20063-146">INPUTS</span></span>

## <span data-ttu-id="20063-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20063-147">OUTPUTS</span></span>

## <span data-ttu-id="20063-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20063-148">NOTES</span></span>

## <span data-ttu-id="20063-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20063-149">RELATED LINKS</span></span>

[<span data-ttu-id="20063-150">Mover-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="20063-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="20063-151">Mover-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="20063-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="20063-152">Mover-AzureService</span><span class="sxs-lookup"><span data-stu-id="20063-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="20063-153">Mover-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20063-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="20063-154">Mover-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20063-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


