---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946240"
---
# <span data-ttu-id="f65ff-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="f65ff-101">Move-AzureService</span></span>

## <span data-ttu-id="f65ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f65ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f65ff-103">Migra um serviço na nuvem para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ff-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f65ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f65ff-104">SYNTAX</span></span>

### <span data-ttu-id="f65ff-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f65ff-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f65ff-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f65ff-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f65ff-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f65ff-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f65ff-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f65ff-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f65ff-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f65ff-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f65ff-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f65ff-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f65ff-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f65ff-111">DESCRIPTION</span></span>
<span data-ttu-id="f65ff-112">O cmdlet **move-AzureService** migra um serviço de nuvem e uma implantação dentro desse serviço para um grupo de recursos na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f65ff-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f65ff-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f65ff-113">EXAMPLES</span></span>

### <span data-ttu-id="f65ff-114">Exemplo 1: preparar a migração de serviços</span><span class="sxs-lookup"><span data-stu-id="f65ff-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="f65ff-115">Esse comando prepara o serviço denominado ContosoService para migração para a pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f65ff-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="f65ff-116">A migração inclui a implantação chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="f65ff-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="f65ff-117">Exemplo 2: iniciar a migração do serviço</span><span class="sxs-lookup"><span data-stu-id="f65ff-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="f65ff-118">Esse comando inicia a migração do serviço chamado ContosoService para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ff-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="f65ff-119">A migração inclui a implantação chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="f65ff-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="f65ff-120">Exemplo 3: cancelar a migração do serviço</span><span class="sxs-lookup"><span data-stu-id="f65ff-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="f65ff-121">Esse comando cancela a migração do serviço denominado ContosoService para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ff-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="f65ff-122">Exemplo 4: preparar a migração do serviço para uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="f65ff-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="f65ff-123">Esse comando prepara o serviço denominado ContosoService para migração para a pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f65ff-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="f65ff-124">A migração inclui a implantação chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="f65ff-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="f65ff-125">A migração usa uma rede virtual que foi criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f65ff-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="f65ff-126">Exemplo 5: validar a migração do serviço</span><span class="sxs-lookup"><span data-stu-id="f65ff-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="f65ff-127">Esse comando valida a migração do serviço denominado ContosoService para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ff-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="f65ff-128">A migração inclui a implantação chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="f65ff-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="f65ff-129">Exemplo 6: validar a migração do serviço para uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="f65ff-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="f65ff-130">Esse comando valida a migração do serviço denominado ContosoService para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ff-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="f65ff-131">A migração inclui a implantação chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="f65ff-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="f65ff-132">A migração usa uma rede virtual que foi criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f65ff-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="f65ff-133">OS</span><span class="sxs-lookup"><span data-stu-id="f65ff-133">PARAMETERS</span></span>

### <span data-ttu-id="f65ff-134">-Abort</span><span class="sxs-lookup"><span data-stu-id="f65ff-134">-Abort</span></span>
<span data-ttu-id="f65ff-135">Indica que esse cmdlet cancela a migração do serviço.</span><span class="sxs-lookup"><span data-stu-id="f65ff-135">Indicates that this cmdlet cancels the service migration.</span></span>

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

### <span data-ttu-id="f65ff-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f65ff-136">-Commit</span></span>
<span data-ttu-id="f65ff-137">Indica que esse cmdlet inicia a migração do serviço.</span><span class="sxs-lookup"><span data-stu-id="f65ff-137">Indicates that this cmdlet starts the service migration.</span></span>

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

### <span data-ttu-id="f65ff-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f65ff-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="f65ff-139">Indica que esse cmdlet cria uma rede virtual na pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ff-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-140">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="f65ff-140">-DeploymentName</span></span>
<span data-ttu-id="f65ff-141">Especifica o nome da implantação do serviço de nuvem que este cmdlet migra.</span><span class="sxs-lookup"><span data-stu-id="f65ff-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-142">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f65ff-142">-InformationAction</span></span>
<span data-ttu-id="f65ff-143">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f65ff-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f65ff-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f65ff-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f65ff-145">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f65ff-145">Continue</span></span>
- <span data-ttu-id="f65ff-146">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f65ff-146">Ignore</span></span>
- <span data-ttu-id="f65ff-147">Inquire</span><span class="sxs-lookup"><span data-stu-id="f65ff-147">Inquire</span></span>
- <span data-ttu-id="f65ff-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f65ff-148">SilentlyContinue</span></span>
- <span data-ttu-id="f65ff-149">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f65ff-149">Stop</span></span>
- <span data-ttu-id="f65ff-150">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f65ff-150">Suspend</span></span>

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

### <span data-ttu-id="f65ff-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f65ff-151">-InformationVariable</span></span>
<span data-ttu-id="f65ff-152">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f65ff-152">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f65ff-153">-Prepare</span><span class="sxs-lookup"><span data-stu-id="f65ff-153">-Prepare</span></span>
<span data-ttu-id="f65ff-154">Indica que esse cmdlet prepara o serviço na nuvem para migração.</span><span class="sxs-lookup"><span data-stu-id="f65ff-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-155">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f65ff-155">-Profile</span></span>
<span data-ttu-id="f65ff-156">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f65ff-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f65ff-157">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f65ff-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f65ff-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f65ff-158">-ServiceName</span></span>
<span data-ttu-id="f65ff-159">Especifica o nome do serviço de nuvem que este cmdlet migra.</span><span class="sxs-lookup"><span data-stu-id="f65ff-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="f65ff-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f65ff-160">-SubnetName</span></span>
<span data-ttu-id="f65ff-161">Especifica o nome da sub-rede dentro da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f65ff-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f65ff-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="f65ff-163">Indica que esse cmdlet migra o serviço na nuvem para uma rede virtual existente na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f65ff-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-164">-Validar</span><span class="sxs-lookup"><span data-stu-id="f65ff-164">-Validate</span></span>
<span data-ttu-id="f65ff-165">Especifica que esse cmdlet valida o serviço na nuvem para migração.</span><span class="sxs-lookup"><span data-stu-id="f65ff-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f65ff-166">-VirtualNetworkName</span></span>
<span data-ttu-id="f65ff-167">Especifica o nome de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f65ff-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65ff-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="f65ff-169">Especifica o nome do grupo de recursos de uma rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="f65ff-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ff-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65ff-170">CommonParameters</span></span>
<span data-ttu-id="f65ff-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65ff-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65ff-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65ff-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65ff-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f65ff-173">INPUTS</span></span>

## <span data-ttu-id="f65ff-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f65ff-174">OUTPUTS</span></span>

## <span data-ttu-id="f65ff-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f65ff-175">NOTES</span></span>

## <span data-ttu-id="f65ff-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f65ff-176">RELATED LINKS</span></span>

[<span data-ttu-id="f65ff-177">Mover-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f65ff-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="f65ff-178">Mover-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="f65ff-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="f65ff-179">Mover-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="f65ff-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="f65ff-180">Mover-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f65ff-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="f65ff-181">Mover-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f65ff-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


