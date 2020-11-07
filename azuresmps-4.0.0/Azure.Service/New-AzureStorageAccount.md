---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946204"
---
# <span data-ttu-id="5f8c7-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5f8c7-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="5f8c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8c7-103">Cria uma nova conta de armazenamento em uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="5f8c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f8c7-104">SYNTAX</span></span>

### <span data-ttu-id="5f8c7-105">ParameterSetAffinityGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f8c7-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5f8c7-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="5f8c7-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5f8c7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f8c7-107">DESCRIPTION</span></span>
<span data-ttu-id="5f8c7-108">O cmdlet **New-AzureStorageAccount** cria uma conta que fornece acesso aos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="5f8c7-109">Uma conta de armazenamento é um recurso globalmente exclusivo no sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="5f8c7-110">A conta é o namespace pai para BLOB, fila e serviços de tabela.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="5f8c7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-111">EXAMPLES</span></span>

### <span data-ttu-id="5f8c7-112">Exemplo 1: criar uma conta de armazenamento para um grupo de afinidade especificado</span><span class="sxs-lookup"><span data-stu-id="5f8c7-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="5f8c7-113">Esse comando cria uma conta de armazenamento para um grupo de afinidade especificado.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="5f8c7-114">Exemplo 2: criar uma conta de armazenamento em um local especificado</span><span class="sxs-lookup"><span data-stu-id="5f8c7-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="5f8c7-115">Esse comando cria uma conta de armazenamento em um local especificado.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="5f8c7-116">OS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-116">PARAMETERS</span></span>

### <span data-ttu-id="5f8c7-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5f8c7-117">-AffinityGroup</span></span>
<span data-ttu-id="5f8c7-118">Especifica o nome de um grupo de afinidade existente na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="5f8c7-119">Você pode especificar o parâmetro *Location* ou *AffinityGroup* , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f8c7-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5f8c7-120">-Description</span></span>
<span data-ttu-id="5f8c7-121">Especifica uma descrição para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="5f8c7-122">A descrição pode ter até 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f8c7-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5f8c7-123">-InformationAction</span></span>
<span data-ttu-id="5f8c7-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5f8c7-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5f8c7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f8c7-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="5f8c7-126">Continue</span></span>
- <span data-ttu-id="5f8c7-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="5f8c7-127">Ignore</span></span>
- <span data-ttu-id="5f8c7-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="5f8c7-128">Inquire</span></span>
- <span data-ttu-id="5f8c7-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5f8c7-129">SilentlyContinue</span></span>
- <span data-ttu-id="5f8c7-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="5f8c7-130">Stop</span></span>
- <span data-ttu-id="5f8c7-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="5f8c7-131">Suspend</span></span>

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

### <span data-ttu-id="5f8c7-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5f8c7-132">-InformationVariable</span></span>
<span data-ttu-id="5f8c7-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5f8c7-134">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="5f8c7-134">-Label</span></span>
<span data-ttu-id="5f8c7-135">Especifica um rótulo para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="5f8c7-136">O rótulo pode ter até 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f8c7-137">-Local</span><span class="sxs-lookup"><span data-stu-id="5f8c7-137">-Location</span></span>
<span data-ttu-id="5f8c7-138">Especifica o local do Azure Data Center em que a conta de armazenamento é criada.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="5f8c7-139">Você pode incluir o parâmetro *Location* ou *AffinityGroup* , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f8c7-140">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5f8c7-140">-Profile</span></span>
<span data-ttu-id="5f8c7-141">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f8c7-142">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f8c7-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5f8c7-143">-StorageAccountName</span></span>
<span data-ttu-id="5f8c7-144">Especifica um nome para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="5f8c7-145">O nome da conta de armazenamento deve ser exclusivo para o Azure e deve ter entre 3 e 24 caracteres de comprimento e usar somente letras minúsculas e números.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f8c7-146">-Digite</span><span class="sxs-lookup"><span data-stu-id="5f8c7-146">-Type</span></span>
<span data-ttu-id="5f8c7-147">Especifica o tipo da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="5f8c7-148">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="5f8c7-148">Valid values are:</span></span>

- <span data-ttu-id="5f8c7-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-149">Standard_LRS</span></span>
- <span data-ttu-id="5f8c7-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-150">Standard_ZRS</span></span>
- <span data-ttu-id="5f8c7-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-151">Standard_GRS</span></span>
- <span data-ttu-id="5f8c7-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-152">Standard_RAGRS</span></span>
- <span data-ttu-id="5f8c7-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-153">Premium_LRS</span></span>

<span data-ttu-id="5f8c7-154">Se esse parâmetro não for especificado, o valor padrão será Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="5f8c7-155">Standard_ZRS ou Premium_LRS contas não podem ser alteradas para outros tipos de conta e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="5f8c7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8c7-156">CommonParameters</span></span>
<span data-ttu-id="5f8c7-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8c7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8c7-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8c7-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8c7-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f8c7-159">INPUTS</span></span>

## <span data-ttu-id="5f8c7-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f8c7-160">OUTPUTS</span></span>

## <span data-ttu-id="5f8c7-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f8c7-161">NOTES</span></span>

## <span data-ttu-id="5f8c7-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f8c7-162">RELATED LINKS</span></span>

[<span data-ttu-id="5f8c7-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5f8c7-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="5f8c7-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5f8c7-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


