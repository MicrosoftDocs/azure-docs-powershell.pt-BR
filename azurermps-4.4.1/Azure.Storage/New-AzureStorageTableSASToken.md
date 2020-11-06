---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611016"
---
# <span data-ttu-id="57c61-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="57c61-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="57c61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57c61-102">SYNOPSIS</span></span>
<span data-ttu-id="57c61-103">Gera um token SAS para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="57c61-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57c61-104">SYNTAX</span></span>

### <span data-ttu-id="57c61-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="57c61-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="57c61-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="57c61-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="57c61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57c61-107">DESCRIPTION</span></span>
<span data-ttu-id="57c61-108">O cmdlet **New-AzureStorageTableSASToken** gera um token de assinatura de acesso compartilhado (SAS) para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="57c61-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="57c61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57c61-109">EXAMPLES</span></span>

### <span data-ttu-id="57c61-110">Exemplo 1: gerar um token SAS com permissões completas para uma tabela</span><span class="sxs-lookup"><span data-stu-id="57c61-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="57c61-111">Esse comando gera um token SAS com permissões completas para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="57c61-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="57c61-112">Esse token é para permissões de leitura, adição, atualização e exclusão.</span><span class="sxs-lookup"><span data-stu-id="57c61-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="57c61-113">Exemplo 2: gerar um token SAS para um intervalo de partições</span><span class="sxs-lookup"><span data-stu-id="57c61-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="57c61-114">Esse comando gera um token SAS com permissões completas para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="57c61-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="57c61-115">O comando limita o token para o intervalo que os parâmetros *StartPartitionKey* e *EndPartitionKey* especificam.</span><span class="sxs-lookup"><span data-stu-id="57c61-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="57c61-116">Exemplo 3: gerar um token SAS com uma política de acesso armazenado para uma tabela</span><span class="sxs-lookup"><span data-stu-id="57c61-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="57c61-117">Esse comando gera um token SAS para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="57c61-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="57c61-118">O comando especifica a política de acesso armazenada chamada ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="57c61-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="57c61-119">OS</span><span class="sxs-lookup"><span data-stu-id="57c61-119">PARAMETERS</span></span>

### <span data-ttu-id="57c61-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="57c61-120">-Context</span></span>
<span data-ttu-id="57c61-121">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="57c61-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="57c61-122">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="57c61-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="57c61-123">-EndPartitionKey</span></span>
<span data-ttu-id="57c61-124">Especifica a chave de partição do final do intervalo para o token criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c61-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="57c61-125">-EndRowKey</span></span>
<span data-ttu-id="57c61-126">Especifica a chave de linha para o final do intervalo do token criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c61-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="57c61-127">-ExpiryTime</span></span>
<span data-ttu-id="57c61-128">Especifica quando o token SAS expira.</span><span class="sxs-lookup"><span data-stu-id="57c61-128">Specifies when the SAS token expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="57c61-129">-FullUri</span></span>
<span data-ttu-id="57c61-130">Indica que esse cmdlet retorna o URI da fila completa com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="57c61-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="57c61-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="57c61-131">-IPAddressOrRange</span></span>
<span data-ttu-id="57c61-132">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="57c61-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="57c61-133">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="57c61-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="57c61-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="57c61-134">-Name</span></span>
<span data-ttu-id="57c61-135">Especifica o nome de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="57c61-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="57c61-136">Esse cmdlet cria um token SAS para a tabela que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="57c61-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-137">-Permissão</span><span class="sxs-lookup"><span data-stu-id="57c61-137">-Permission</span></span>
<span data-ttu-id="57c61-138">Especifica permissões para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="57c61-138">Specifies permissions for an Azure Storage table.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-139">-Política</span><span class="sxs-lookup"><span data-stu-id="57c61-139">-Policy</span></span>
<span data-ttu-id="57c61-140">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="57c61-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-141">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="57c61-141">-Protocol</span></span>
<span data-ttu-id="57c61-142">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="57c61-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="57c61-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="57c61-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="57c61-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="57c61-144">HttpsOnly</span></span>
* <span data-ttu-id="57c61-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="57c61-145">HttpsOrHttp</span></span>

<span data-ttu-id="57c61-146">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="57c61-146">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="57c61-147">-StartPartitionKey</span></span>
<span data-ttu-id="57c61-148">Especifica a chave de partição do início do intervalo para o token criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c61-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="57c61-149">-StartRowKey</span></span>
<span data-ttu-id="57c61-150">Especifica a chave de linha para o início do intervalo para o token que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="57c61-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="57c61-151">-StartTime</span></span>
<span data-ttu-id="57c61-152">Especifica quando o token SAS se torna válido.</span><span class="sxs-lookup"><span data-stu-id="57c61-152">Specifies when the SAS token becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c61-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c61-153">CommonParameters</span></span>
<span data-ttu-id="57c61-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c61-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c61-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c61-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c61-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57c61-156">INPUTS</span></span>

### <span data-ttu-id="57c61-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="57c61-157">IStorageContext</span></span>

<span data-ttu-id="57c61-158">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="57c61-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="57c61-159">String</span><span class="sxs-lookup"><span data-stu-id="57c61-159">String</span></span>

<span data-ttu-id="57c61-160">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="57c61-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="57c61-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57c61-161">OUTPUTS</span></span>

### <span data-ttu-id="57c61-162">System. String</span><span class="sxs-lookup"><span data-stu-id="57c61-162">System.String</span></span>

## <span data-ttu-id="57c61-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57c61-163">NOTES</span></span>

## <span data-ttu-id="57c61-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57c61-164">RELATED LINKS</span></span>

[<span data-ttu-id="57c61-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="57c61-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
