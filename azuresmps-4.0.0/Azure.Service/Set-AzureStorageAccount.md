---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945850"
---
# <span data-ttu-id="89f66-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89f66-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="89f66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89f66-102">SYNOPSIS</span></span>
<span data-ttu-id="89f66-103">Atualiza as propriedades de uma conta de armazenamento em uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="89f66-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="89f66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89f66-104">SYNTAX</span></span>

### <span data-ttu-id="89f66-105">AccountType (padrão)</span><span class="sxs-lookup"><span data-stu-id="89f66-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89f66-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="89f66-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89f66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89f66-107">DESCRIPTION</span></span>
<span data-ttu-id="89f66-108">O cmdlet **set-AzureStorageAccount** atualiza as propriedades de uma conta de armazenamento do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="89f66-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="89f66-109">As propriedades que podem ser definidas são: **rótulo** , **Descrição** , **tipo** e **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="89f66-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="89f66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89f66-110">EXAMPLES</span></span>

### <span data-ttu-id="89f66-111">Exemplo 1: atualizar o rótulo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="89f66-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="89f66-112">Esse comando atualiza as propriedades **rótulo** e **Descrição** da conta de armazenamento chamada ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="89f66-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="89f66-113">Exemplo 2: habilitar a replicação geográfica para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="89f66-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="89f66-114">Esse comando define a propriedade **GeoReplicationEnabled** como $false para a conta de armazenamento chamada ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="89f66-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="89f66-115">Exemplo 3: desabilitar a replicação geográfica para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="89f66-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="89f66-116">Esse comando define a propriedade **GeoReplicationEnabled** como $true para a conta de armazenamento chamada ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="89f66-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="89f66-117">OS</span><span class="sxs-lookup"><span data-stu-id="89f66-117">PARAMETERS</span></span>

### <span data-ttu-id="89f66-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="89f66-118">-Description</span></span>
<span data-ttu-id="89f66-119">Especifica uma descrição para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="89f66-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="89f66-120">A descrição pode ter até 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="89f66-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="89f66-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="89f66-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="89f66-122">Especifica se a conta de armazenamento é criada com a replicação geográfica habilitada.</span><span class="sxs-lookup"><span data-stu-id="89f66-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f66-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="89f66-123">-InformationAction</span></span>
<span data-ttu-id="89f66-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="89f66-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89f66-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="89f66-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89f66-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="89f66-126">Continue</span></span>
- <span data-ttu-id="89f66-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="89f66-127">Ignore</span></span>
- <span data-ttu-id="89f66-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="89f66-128">Inquire</span></span>
- <span data-ttu-id="89f66-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89f66-129">SilentlyContinue</span></span>
- <span data-ttu-id="89f66-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="89f66-130">Stop</span></span>
- <span data-ttu-id="89f66-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="89f66-131">Suspend</span></span>

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

### <span data-ttu-id="89f66-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89f66-132">-InformationVariable</span></span>
<span data-ttu-id="89f66-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="89f66-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="89f66-134">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="89f66-134">-Label</span></span>
<span data-ttu-id="89f66-135">Especifica um rótulo para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="89f66-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="89f66-136">O rótulo pode ter até 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="89f66-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="89f66-137">-Perfil</span><span class="sxs-lookup"><span data-stu-id="89f66-137">-Profile</span></span>
<span data-ttu-id="89f66-138">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="89f66-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89f66-139">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="89f66-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89f66-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89f66-140">-StorageAccountName</span></span>
<span data-ttu-id="89f66-141">Especifica o nome da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="89f66-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f66-142">-Digite</span><span class="sxs-lookup"><span data-stu-id="89f66-142">-Type</span></span>
<span data-ttu-id="89f66-143">Especifica o tipo da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="89f66-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="89f66-144">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="89f66-144">Valid values are:</span></span> 

- <span data-ttu-id="89f66-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="89f66-145">Standard_LRS</span></span>
- <span data-ttu-id="89f66-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="89f66-146">Standard_ZRS</span></span>
- <span data-ttu-id="89f66-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="89f66-147">Standard_GRS</span></span>
- <span data-ttu-id="89f66-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="89f66-148">Standard_RAGRS</span></span>
- <span data-ttu-id="89f66-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="89f66-149">Premium_LRS</span></span>

<span data-ttu-id="89f66-150">Se esse parâmetro não for especificado, o valor padrão será Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="89f66-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="89f66-151">O efeito de especificar o parâmetro *GeoReplicationEnabled* é o mesmo que especificar Standard_GRS no parâmetro *Type* .</span><span class="sxs-lookup"><span data-stu-id="89f66-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="89f66-152">Standard_ZRS ou Premium_LRS contas não podem ser alteradas para outros tipos de conta e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="89f66-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f66-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f66-153">CommonParameters</span></span>
<span data-ttu-id="89f66-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f66-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f66-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f66-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f66-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89f66-156">INPUTS</span></span>

## <span data-ttu-id="89f66-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89f66-157">OUTPUTS</span></span>

## <span data-ttu-id="89f66-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89f66-158">NOTES</span></span>

## <span data-ttu-id="89f66-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89f66-159">RELATED LINKS</span></span>

[<span data-ttu-id="89f66-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89f66-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="89f66-161">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89f66-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="89f66-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89f66-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


