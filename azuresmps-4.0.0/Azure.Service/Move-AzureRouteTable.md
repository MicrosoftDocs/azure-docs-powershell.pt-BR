---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946241"
---
# <span data-ttu-id="b4efc-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4efc-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="b4efc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4efc-102">SYNOPSIS</span></span>
<span data-ttu-id="b4efc-103">Migra uma tabela de rota para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4efc-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4efc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4efc-104">SYNTAX</span></span>

### <span data-ttu-id="b4efc-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4efc-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4efc-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4efc-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4efc-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4efc-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4efc-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4efc-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4efc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4efc-109">DESCRIPTION</span></span>
<span data-ttu-id="b4efc-110">O cmdlet **move-AzureRouteTable** migra uma tabela de rota para um grupo de recursos na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b4efc-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4efc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4efc-111">EXAMPLES</span></span>

### <span data-ttu-id="b4efc-112">1:</span><span class="sxs-lookup"><span data-stu-id="b4efc-112">1:</span></span>
```

```

## <span data-ttu-id="b4efc-113">OS</span><span class="sxs-lookup"><span data-stu-id="b4efc-113">PARAMETERS</span></span>

### <span data-ttu-id="b4efc-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="b4efc-114">-Abort</span></span>
<span data-ttu-id="b4efc-115">Indica que esse cmdlet cancela a migração da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="b4efc-115">Indicates that this cmdlet cancels the route table migration.</span></span>

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

### <span data-ttu-id="b4efc-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4efc-116">-Commit</span></span>
<span data-ttu-id="b4efc-117">Indica que esse cmdlet inicia a migração da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="b4efc-117">Indicates that this cmdlet starts the route table migration.</span></span>

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

### <span data-ttu-id="b4efc-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b4efc-118">-InformationAction</span></span>
<span data-ttu-id="b4efc-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b4efc-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4efc-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b4efc-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4efc-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b4efc-121">Continue</span></span>
- <span data-ttu-id="b4efc-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b4efc-122">Ignore</span></span>
- <span data-ttu-id="b4efc-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="b4efc-123">Inquire</span></span>
- <span data-ttu-id="b4efc-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4efc-124">SilentlyContinue</span></span>
- <span data-ttu-id="b4efc-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b4efc-125">Stop</span></span>
- <span data-ttu-id="b4efc-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b4efc-126">Suspend</span></span>

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

### <span data-ttu-id="b4efc-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4efc-127">-InformationVariable</span></span>
<span data-ttu-id="b4efc-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b4efc-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4efc-129">-Prepare</span><span class="sxs-lookup"><span data-stu-id="b4efc-129">-Prepare</span></span>
<span data-ttu-id="b4efc-130">Indica que esse cmdlet prepara a tabela de rota para a migração.</span><span class="sxs-lookup"><span data-stu-id="b4efc-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

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

### <span data-ttu-id="b4efc-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b4efc-131">-Profile</span></span>
<span data-ttu-id="b4efc-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b4efc-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4efc-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b4efc-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4efc-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="b4efc-134">-RouteTableName</span></span>
<span data-ttu-id="b4efc-135">Especifica o nome da tabela de rota que este cmdlet migra.</span><span class="sxs-lookup"><span data-stu-id="b4efc-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="b4efc-136">-Validar</span><span class="sxs-lookup"><span data-stu-id="b4efc-136">-Validate</span></span>
<span data-ttu-id="b4efc-137">Especifica que esse cmdlet valida a tabela de rota para a migração.</span><span class="sxs-lookup"><span data-stu-id="b4efc-137">Specifies that this cmdlet validates the route table for migration.</span></span>

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

### <span data-ttu-id="b4efc-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4efc-138">-Confirm</span></span>
<span data-ttu-id="b4efc-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4efc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4efc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4efc-140">-WhatIf</span></span>
<span data-ttu-id="b4efc-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4efc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4efc-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4efc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4efc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4efc-143">CommonParameters</span></span>
<span data-ttu-id="b4efc-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4efc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4efc-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4efc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4efc-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4efc-146">INPUTS</span></span>

## <span data-ttu-id="b4efc-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4efc-147">OUTPUTS</span></span>

## <span data-ttu-id="b4efc-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4efc-148">NOTES</span></span>

## <span data-ttu-id="b4efc-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4efc-149">RELATED LINKS</span></span>

[<span data-ttu-id="b4efc-150">Mover-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4efc-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b4efc-151">Mover-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b4efc-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="b4efc-152">Mover-AzureService</span><span class="sxs-lookup"><span data-stu-id="b4efc-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="b4efc-153">Mover-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4efc-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="b4efc-154">Mover-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4efc-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


