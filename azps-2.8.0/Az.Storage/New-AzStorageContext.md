---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: eca1322f1638039fce6c478b19e94b586fd83bbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774195"
---
# <span data-ttu-id="f0b25-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0b25-101">New-AzStorageContext</span></span>

## <span data-ttu-id="f0b25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0b25-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b25-103">Cria um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="f0b25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0b25-104">SYNTAX</span></span>

### <span data-ttu-id="f0b25-105">OAuthAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="f0b25-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0b25-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="f0b25-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0b25-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0b25-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="f0b25-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="f0b25-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0b25-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0b25-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="f0b25-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="f0b25-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0b25-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0b25-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="f0b25-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="f0b25-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="f0b25-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f0b25-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="f0b25-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="f0b25-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="f0b25-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0b25-115">DESCRIPTION</span></span>
<span data-ttu-id="f0b25-116">O cmdlet **New-AzStorageContext** cria um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="f0b25-117">A autenticação padrão de um contexto de armazenamento é a OAuth (Azure AD), se apenas o nome da conta de armazenamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="f0b25-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="f0b25-118">Veja os detalhes da autenticação do serviço de armazenamento em https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="f0b25-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="f0b25-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0b25-119">EXAMPLES</span></span>

### <span data-ttu-id="f0b25-120">Exemplo 1: criar um contexto especificando um nome e uma chave de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f0b25-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="f0b25-121">Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="f0b25-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f0b25-122">Exemplo 2: criar um contexto especificando uma cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="f0b25-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="f0b25-123">Esse comando cria um contexto com base na cadeia de conexão especificada para a conta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="f0b25-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="f0b25-124">Exemplo 3: criar um contexto para uma conta de armazenamento anônimo</span><span class="sxs-lookup"><span data-stu-id="f0b25-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="f0b25-125">Esse comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="f0b25-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="f0b25-126">O comando especifica HTTP como um protocolo de conexão.</span><span class="sxs-lookup"><span data-stu-id="f0b25-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="f0b25-127">Exemplo 4: criar um contexto usando a conta de armazenamento de desenvolvimento local</span><span class="sxs-lookup"><span data-stu-id="f0b25-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="f0b25-128">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="f0b25-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="f0b25-129">O comando especifica o parâmetro *local* .</span><span class="sxs-lookup"><span data-stu-id="f0b25-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="f0b25-130">Exemplo 5: obter o contêiner para a conta de armazenamento do desenvolvedor local</span><span class="sxs-lookup"><span data-stu-id="f0b25-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="f0b25-131">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, passa o novo contexto para o cmdlet **Get-AzStorageContainer** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f0b25-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f0b25-132">O comando obtém o contêiner de armazenamento do Azure para a conta de armazenamento do desenvolvedor local.</span><span class="sxs-lookup"><span data-stu-id="f0b25-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="f0b25-133">Exemplo 6: obter vários contêineres</span><span class="sxs-lookup"><span data-stu-id="f0b25-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="f0b25-134">O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, armazena esse contexto na variável $Context 01.</span><span class="sxs-lookup"><span data-stu-id="f0b25-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="f0b25-135">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e, em seguida, armazena esse contexto na variável $Context 02.</span><span class="sxs-lookup"><span data-stu-id="f0b25-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="f0b25-136">O comando final Obtém os contêineres para os contextos armazenados em $Context 01 e $Context 02 usando **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="f0b25-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="f0b25-137">Exemplo 7: criar um contexto com um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="f0b25-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="f0b25-138">Esse comando cria um contexto de armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="f0b25-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="f0b25-139">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="f0b25-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f0b25-140">Exemplo 8: criar um contexto com um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="f0b25-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="f0b25-141">Esse comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="f0b25-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="f0b25-142">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="f0b25-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="f0b25-143">Exemplo 9: criar um contexto usando um token SAS</span><span class="sxs-lookup"><span data-stu-id="f0b25-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="f0b25-144">O primeiro comando gera um token SAS usando o cmdlet **New-AzStorageContainerSASToken** para o contêiner chamado ContosoMain e, em seguida, armazena esse token na variável $SasToken.</span><span class="sxs-lookup"><span data-stu-id="f0b25-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="f0b25-145">Esse token é para permissões de leitura, adição, atualização e exclusão.</span><span class="sxs-lookup"><span data-stu-id="f0b25-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="f0b25-146">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e, em seguida, armazena esse contexto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="f0b25-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="f0b25-147">O comando final lista todos os BLOBs associados ao contêiner nomeado ContosoMain usando o contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="f0b25-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="f0b25-148">Exemplo 10: criar um contexto usando a autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="f0b25-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="f0b25-149">Esse comando cria um contexto usando a autenticação OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f0b25-149">This command creates a context by using the OAuth (Azure AD)  Authentication.</span></span>

## <span data-ttu-id="f0b25-150">OS</span><span class="sxs-lookup"><span data-stu-id="f0b25-150">PARAMETERS</span></span>

### <span data-ttu-id="f0b25-151">-Anônimo</span><span class="sxs-lookup"><span data-stu-id="f0b25-151">-Anonymous</span></span>
<span data-ttu-id="f0b25-152">Indica que esse cmdlet cria um contexto de armazenamento do Azure para logon anônimo.</span><span class="sxs-lookup"><span data-stu-id="f0b25-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f0b25-153">-ConnectionString</span></span>
<span data-ttu-id="f0b25-154">Especifica uma cadeia de conexão para o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-155">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="f0b25-155">-Endpoint</span></span>
<span data-ttu-id="f0b25-156">Especifica o ponto de extremidade para o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-157">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="f0b25-157">-Environment</span></span>
<span data-ttu-id="f0b25-158">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="f0b25-159">Os valores aceitáveis para esse parâmetro são: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="f0b25-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="f0b25-160">Para obter mais informações, digite `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="f0b25-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-161">-Local</span><span class="sxs-lookup"><span data-stu-id="f0b25-161">-Local</span></span>
<span data-ttu-id="f0b25-162">Indica que esse cmdlet cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="f0b25-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-163">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f0b25-163">-Protocol</span></span>
<span data-ttu-id="f0b25-164">Protocolo de transferência (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="f0b25-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="f0b25-165">-SasToken</span></span>
<span data-ttu-id="f0b25-166">Especifica um token de assinatura de acesso compartilhado (SAS) para o contexto.</span><span class="sxs-lookup"><span data-stu-id="f0b25-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f0b25-167">-StorageAccountKey</span></span>
<span data-ttu-id="f0b25-168">Especifica uma chave de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="f0b25-169">Esse cmdlet cria um contexto para a chave que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f0b25-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f0b25-170">-StorageAccountName</span></span>
<span data-ttu-id="f0b25-171">Especifica um nome de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b25-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="f0b25-172">Esse cmdlet cria um contexto para a conta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f0b25-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="f0b25-173">-UseConnectedAccount</span></span>
<span data-ttu-id="f0b25-174">Indica que esse cmdlet cria um contexto de armazenamento do Azure com Autenticação OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f0b25-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="f0b25-175">O cmdlet usará a autenticação OAuth por padrão, quando outra autenticação não for especificada.</span><span class="sxs-lookup"><span data-stu-id="f0b25-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b25-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b25-176">CommonParameters</span></span>
<span data-ttu-id="f0b25-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b25-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b25-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b25-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b25-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0b25-179">INPUTS</span></span>

### <span data-ttu-id="f0b25-180">System. String</span><span class="sxs-lookup"><span data-stu-id="f0b25-180">System.String</span></span>

## <span data-ttu-id="f0b25-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0b25-181">OUTPUTS</span></span>

### <span data-ttu-id="f0b25-182">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0b25-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="f0b25-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0b25-183">NOTES</span></span>

## <span data-ttu-id="f0b25-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0b25-184">RELATED LINKS</span></span>

[<span data-ttu-id="f0b25-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f0b25-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="f0b25-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f0b25-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


