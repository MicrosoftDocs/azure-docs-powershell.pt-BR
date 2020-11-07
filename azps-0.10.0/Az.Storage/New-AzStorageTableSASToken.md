---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 190db8ff50c3c52fb8d43a2cdbd509f9e67ea63b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776207"
---
# <span data-ttu-id="d656c-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="d656c-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="d656c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d656c-102">SYNOPSIS</span></span>
<span data-ttu-id="d656c-103">Gera um token SAS para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d656c-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="d656c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d656c-104">SYNTAX</span></span>

### <span data-ttu-id="d656c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d656c-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d656c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d656c-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d656c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d656c-107">DESCRIPTION</span></span>
<span data-ttu-id="d656c-108">O cmdlet **New-AzStorageTableSASToken** gera um token de assinatura de acesso compartilhado (SAS) para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d656c-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="d656c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d656c-109">EXAMPLES</span></span>

### <span data-ttu-id="d656c-110">Exemplo 1: gerar um token SAS com permissões completas para uma tabela</span><span class="sxs-lookup"><span data-stu-id="d656c-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="d656c-111">Esse comando gera um token SAS com permissões completas para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="d656c-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="d656c-112">Esse token é para permissões de leitura, adição, atualização e exclusão.</span><span class="sxs-lookup"><span data-stu-id="d656c-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="d656c-113">Exemplo 2: gerar um token SAS para um intervalo de partições</span><span class="sxs-lookup"><span data-stu-id="d656c-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="d656c-114">Esse comando gera um token SAS com permissões completas para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="d656c-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="d656c-115">O comando limita o token para o intervalo que os parâmetros *StartPartitionKey* e *EndPartitionKey* especificam.</span><span class="sxs-lookup"><span data-stu-id="d656c-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="d656c-116">Exemplo 3: gerar um token SAS com uma política de acesso armazenado para uma tabela</span><span class="sxs-lookup"><span data-stu-id="d656c-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="d656c-117">Esse comando gera um token SAS para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="d656c-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="d656c-118">O comando especifica a política de acesso armazenada chamada ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="d656c-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="d656c-119">OS</span><span class="sxs-lookup"><span data-stu-id="d656c-119">PARAMETERS</span></span>

### <span data-ttu-id="d656c-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d656c-120">-Context</span></span>
<span data-ttu-id="d656c-121">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d656c-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d656c-122">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d656c-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d656c-123">-DefaultProfile</span></span>
<span data-ttu-id="d656c-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d656c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="d656c-125">-EndPartitionKey</span></span>
<span data-ttu-id="d656c-126">Especifica a chave de partição do final do intervalo para o token criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d656c-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="d656c-127">-EndRowKey</span></span>
<span data-ttu-id="d656c-128">Especifica a chave de linha para o final do intervalo do token criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d656c-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d656c-129">-ExpiryTime</span></span>
<span data-ttu-id="d656c-130">Especifica quando o token SAS expira.</span><span class="sxs-lookup"><span data-stu-id="d656c-130">Specifies when the SAS token expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d656c-131">-FullUri</span></span>
<span data-ttu-id="d656c-132">Indica que esse cmdlet retorna o URI da fila completa com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="d656c-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d656c-133">-IPAddressOrRange</span></span>
<span data-ttu-id="d656c-134">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d656c-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d656c-135">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="d656c-135">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="d656c-136">-Name</span></span>
<span data-ttu-id="d656c-137">Especifica o nome de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d656c-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="d656c-138">Esse cmdlet cria um token SAS para a tabela que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d656c-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-139">-Permissão</span><span class="sxs-lookup"><span data-stu-id="d656c-139">-Permission</span></span>
<span data-ttu-id="d656c-140">Especifica permissões para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d656c-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="d656c-141">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="d656c-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-142">-Política</span><span class="sxs-lookup"><span data-stu-id="d656c-142">-Policy</span></span>
<span data-ttu-id="d656c-143">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="d656c-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-144">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d656c-144">-Protocol</span></span>
<span data-ttu-id="d656c-145">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d656c-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d656c-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d656c-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d656c-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d656c-147">HttpsOnly</span></span>
* <span data-ttu-id="d656c-148">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d656c-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="d656c-149">-StartPartitionKey</span></span>
<span data-ttu-id="d656c-150">Especifica a chave de partição do início do intervalo para o token criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d656c-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="d656c-151">-StartRowKey</span></span>
<span data-ttu-id="d656c-152">Especifica a chave de linha para o início do intervalo para o token que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d656c-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d656c-153">-StartTime</span></span>
<span data-ttu-id="d656c-154">Especifica quando o token SAS se torna válido.</span><span class="sxs-lookup"><span data-stu-id="d656c-154">Specifies when the SAS token becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d656c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d656c-155">CommonParameters</span></span>
<span data-ttu-id="d656c-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d656c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d656c-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d656c-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d656c-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d656c-158">INPUTS</span></span>

### <span data-ttu-id="d656c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="d656c-159">System.String</span></span>

### <span data-ttu-id="d656c-160">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d656c-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d656c-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d656c-161">OUTPUTS</span></span>

### <span data-ttu-id="d656c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="d656c-162">System.String</span></span>

## <span data-ttu-id="d656c-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d656c-163">NOTES</span></span>

## <span data-ttu-id="d656c-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d656c-164">RELATED LINKS</span></span>

[<span data-ttu-id="d656c-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d656c-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
