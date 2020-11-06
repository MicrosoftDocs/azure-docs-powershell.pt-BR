---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425980"
---
# <span data-ttu-id="d30a6-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d30a6-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="d30a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d30a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d30a6-103">Cria um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="d30a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d30a6-104">SYNTAX</span></span>

### <span data-ttu-id="d30a6-105">AccountNameAndKey (padrão)</span><span class="sxs-lookup"><span data-stu-id="d30a6-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d30a6-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="d30a6-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d30a6-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="d30a6-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d30a6-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d30a6-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d30a6-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="d30a6-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d30a6-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d30a6-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d30a6-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d30a6-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="d30a6-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="d30a6-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="d30a6-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d30a6-113">DESCRIPTION</span></span>
<span data-ttu-id="d30a6-114">O cmdlet **New-AzureStorageContext** cria um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="d30a6-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d30a6-115">EXAMPLES</span></span>

### <span data-ttu-id="d30a6-116">Exemplo 1: criar um contexto especificando um nome e uma chave de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d30a6-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="d30a6-117">Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="d30a6-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d30a6-118">Exemplo 2: criar um contexto especificando uma cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="d30a6-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="d30a6-119">Esse comando cria um contexto com base na cadeia de conexão especificada para a conta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d30a6-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="d30a6-120">Exemplo 3: criar um contexto para uma conta de armazenamento anônimo</span><span class="sxs-lookup"><span data-stu-id="d30a6-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="d30a6-121">Esse comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="d30a6-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="d30a6-122">O comando especifica HTTP como um protocolo de conexão.</span><span class="sxs-lookup"><span data-stu-id="d30a6-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="d30a6-123">Exemplo 4: criar um contexto usando a conta de armazenamento de desenvolvimento local</span><span class="sxs-lookup"><span data-stu-id="d30a6-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="d30a6-124">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="d30a6-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="d30a6-125">O comando especifica o parâmetro *local* .</span><span class="sxs-lookup"><span data-stu-id="d30a6-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="d30a6-126">Exemplo 5: obter o contêiner para a conta de armazenamento do desenvolvedor local</span><span class="sxs-lookup"><span data-stu-id="d30a6-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="d30a6-127">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, passa o novo contexto para o cmdlet **Get-AzureStorageContainer** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d30a6-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d30a6-128">O comando obtém o contêiner de armazenamento do Azure para a conta de armazenamento do desenvolvedor local.</span><span class="sxs-lookup"><span data-stu-id="d30a6-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="d30a6-129">Exemplo 6: obter vários contêineres</span><span class="sxs-lookup"><span data-stu-id="d30a6-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="d30a6-130">O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, armazena esse contexto na variável $Context 01.</span><span class="sxs-lookup"><span data-stu-id="d30a6-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="d30a6-131">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e, em seguida, armazena esse contexto na variável $Context 02.</span><span class="sxs-lookup"><span data-stu-id="d30a6-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="d30a6-132">O comando final Obtém os contêineres para os contextos armazenados em $Context 01 e $Context 02 usando **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="d30a6-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="d30a6-133">Exemplo 7: criar um contexto com um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="d30a6-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="d30a6-134">Esse comando cria um contexto de armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d30a6-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="d30a6-135">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="d30a6-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d30a6-136">Exemplo 8: criar um contexto com um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="d30a6-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="d30a6-137">Esse comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="d30a6-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="d30a6-138">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="d30a6-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d30a6-139">Exemplo 9: criar um contexto usando um token SAS</span><span class="sxs-lookup"><span data-stu-id="d30a6-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="d30a6-140">O primeiro comando gera um token SAS usando o cmdlet **New-AzureStorageContainerSASToken** para o contêiner chamado ContosoMain e, em seguida, armazena esse token na variável $SasToken.</span><span class="sxs-lookup"><span data-stu-id="d30a6-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="d30a6-141">Esse token é para permissões de leitura, adição, atualização e exclusão.</span><span class="sxs-lookup"><span data-stu-id="d30a6-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="d30a6-142">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e, em seguida, armazena esse contexto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="d30a6-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="d30a6-143">O comando final lista todos os BLOBs associados ao contêiner nomeado ContosoMain usando o contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="d30a6-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="d30a6-144">OS</span><span class="sxs-lookup"><span data-stu-id="d30a6-144">PARAMETERS</span></span>

### <span data-ttu-id="d30a6-145">-Anônimo</span><span class="sxs-lookup"><span data-stu-id="d30a6-145">-Anonymous</span></span>
<span data-ttu-id="d30a6-146">Indica que esse cmdlet cria um contexto de armazenamento do Azure para logon anônimo.</span><span class="sxs-lookup"><span data-stu-id="d30a6-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d30a6-147">-ConnectionString</span></span>
<span data-ttu-id="d30a6-148">Especifica uma cadeia de conexão para o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-149">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="d30a6-149">-Endpoint</span></span>
<span data-ttu-id="d30a6-150">Especifica o ponto de extremidade para o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-151">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="d30a6-151">-Environment</span></span>
<span data-ttu-id="d30a6-152">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="d30a6-153">Os valores aceitáveis para esse parâmetro são: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="d30a6-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="d30a6-154">Para obter mais informações, digite `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="d30a6-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-155">-Local</span><span class="sxs-lookup"><span data-stu-id="d30a6-155">-Local</span></span>
<span data-ttu-id="d30a6-156">Indica que esse cmdlet cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="d30a6-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-157">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d30a6-157">-Protocol</span></span>
<span data-ttu-id="d30a6-158">Especifica o protocolo permitido para uma solicitação feita com a SAS da conta.</span><span class="sxs-lookup"><span data-stu-id="d30a6-158">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="d30a6-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d30a6-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d30a6-160">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d30a6-160">HttpsOnly</span></span>
- <span data-ttu-id="d30a6-161">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="d30a6-161">HttpsOrHttp</span></span>

<span data-ttu-id="d30a6-162">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d30a6-162">The default value is HttpsOrHttp.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d30a6-163">-SasToken</span></span>
<span data-ttu-id="d30a6-164">Especifica um token de assinatura de acesso compartilhado (SAS) para o contexto.</span><span class="sxs-lookup"><span data-stu-id="d30a6-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d30a6-165">-StorageAccountKey</span></span>
<span data-ttu-id="d30a6-166">Especifica uma chave de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="d30a6-167">Esse cmdlet cria um contexto para a chave que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d30a6-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d30a6-168">-StorageAccountName</span></span>
<span data-ttu-id="d30a6-169">Especifica um nome de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d30a6-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="d30a6-170">Esse cmdlet cria um contexto para a conta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d30a6-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d30a6-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30a6-171">CommonParameters</span></span>
<span data-ttu-id="d30a6-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d30a6-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30a6-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d30a6-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30a6-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d30a6-174">INPUTS</span></span>

## <span data-ttu-id="d30a6-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d30a6-175">OUTPUTS</span></span>

### <span data-ttu-id="d30a6-176">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d30a6-176">AzureStorageContext</span></span>

## <span data-ttu-id="d30a6-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d30a6-177">NOTES</span></span>

## <span data-ttu-id="d30a6-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d30a6-178">RELATED LINKS</span></span>

[<span data-ttu-id="d30a6-179">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d30a6-179">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="d30a6-180">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d30a6-180">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


