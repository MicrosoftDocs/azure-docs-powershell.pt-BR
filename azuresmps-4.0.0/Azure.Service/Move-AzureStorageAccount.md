---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946239"
---
# <span data-ttu-id="a0849-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0849-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="a0849-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0849-102">SYNOPSIS</span></span>
<span data-ttu-id="a0849-103">Migra uma conta de armazenamento para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0849-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a0849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0849-104">SYNTAX</span></span>

### <span data-ttu-id="a0849-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0849-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0849-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0849-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0849-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0849-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0849-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0849-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a0849-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0849-109">DESCRIPTION</span></span>
<span data-ttu-id="a0849-110">O cmdlet **move-AzureStorageAccount** migra uma conta de armazenamento para um grupo de recursos na pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a0849-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a0849-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0849-111">EXAMPLES</span></span>

### <span data-ttu-id="a0849-112">Exemplo 1: preparar a migração da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a0849-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="a0849-113">Esse comando prepara a conta de armazenamento chamada ContosoStorageName para migração para a pilha do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a0849-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="a0849-114">Exemplo 2: iniciar a migração da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a0849-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="a0849-115">Esse comando inicia a migração da conta de armazenamento chamada ContosoStorageName para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0849-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="a0849-116">Exemplo 3: validar a migração da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a0849-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="a0849-117">Esse comando valida a migração da conta de armazenamento chamada ContosoStorageName para a pilha do Gerenciador de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0849-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a0849-118">OS</span><span class="sxs-lookup"><span data-stu-id="a0849-118">PARAMETERS</span></span>

### <span data-ttu-id="a0849-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="a0849-119">-Abort</span></span>
<span data-ttu-id="a0849-120">Indica que esse cmdlet cancela a migração da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a0849-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

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

### <span data-ttu-id="a0849-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a0849-121">-Commit</span></span>
<span data-ttu-id="a0849-122">Indica que esse cmdlet inicia a migração da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a0849-122">Indicates that this cmdlet starts the storage account migration.</span></span>

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

### <span data-ttu-id="a0849-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a0849-123">-InformationAction</span></span>
<span data-ttu-id="a0849-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a0849-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a0849-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a0849-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0849-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a0849-126">Continue</span></span>
- <span data-ttu-id="a0849-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a0849-127">Ignore</span></span>
- <span data-ttu-id="a0849-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="a0849-128">Inquire</span></span>
- <span data-ttu-id="a0849-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a0849-129">SilentlyContinue</span></span>
- <span data-ttu-id="a0849-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a0849-130">Stop</span></span>
- <span data-ttu-id="a0849-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a0849-131">Suspend</span></span>

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

### <span data-ttu-id="a0849-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a0849-132">-InformationVariable</span></span>
<span data-ttu-id="a0849-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a0849-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a0849-134">-Prepare</span><span class="sxs-lookup"><span data-stu-id="a0849-134">-Prepare</span></span>
<span data-ttu-id="a0849-135">Indica que esse cmdlet prepara a conta de armazenamento para migração.</span><span class="sxs-lookup"><span data-stu-id="a0849-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

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

### <span data-ttu-id="a0849-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a0849-136">-Profile</span></span>
<span data-ttu-id="a0849-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a0849-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0849-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a0849-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0849-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a0849-139">-StorageAccountName</span></span>
<span data-ttu-id="a0849-140">Especifica o nome da conta de armazenamento que este cmdlet migra.</span><span class="sxs-lookup"><span data-stu-id="a0849-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="a0849-141">-Validar</span><span class="sxs-lookup"><span data-stu-id="a0849-141">-Validate</span></span>
<span data-ttu-id="a0849-142">Especifica que esse cmdlet valida a conta de armazenamento para migração.</span><span class="sxs-lookup"><span data-stu-id="a0849-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

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

### <span data-ttu-id="a0849-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0849-143">CommonParameters</span></span>
<span data-ttu-id="a0849-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0849-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0849-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0849-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0849-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0849-146">INPUTS</span></span>

## <span data-ttu-id="a0849-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0849-147">OUTPUTS</span></span>

## <span data-ttu-id="a0849-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0849-148">NOTES</span></span>

## <span data-ttu-id="a0849-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0849-149">RELATED LINKS</span></span>

[<span data-ttu-id="a0849-150">Mover-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a0849-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="a0849-151">Mover-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="a0849-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="a0849-152">Mover-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a0849-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="a0849-153">Mover-AzureService</span><span class="sxs-lookup"><span data-stu-id="a0849-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="a0849-154">Mover-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a0849-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


