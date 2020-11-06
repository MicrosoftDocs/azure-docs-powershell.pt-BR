---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4c506906be76582a77d4a51ae7f103968060b451
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598614"
---
# <span data-ttu-id="19a91-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="19a91-101">New-AzStorageContext</span></span>

## <span data-ttu-id="19a91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19a91-102">SYNOPSIS</span></span>
<span data-ttu-id="19a91-103">Cria um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="19a91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19a91-104">SYNTAX</span></span>

### <span data-ttu-id="19a91-105">OAuthAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="19a91-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="19a91-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="19a91-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="19a91-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="19a91-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="19a91-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="19a91-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="19a91-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="19a91-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="19a91-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="19a91-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="19a91-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="19a91-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="19a91-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="19a91-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="19a91-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="19a91-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="19a91-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="19a91-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="19a91-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19a91-115">DESCRIPTION</span></span>
<span data-ttu-id="19a91-116">O cmdlet **New-AzStorageContext** cria um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="19a91-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19a91-117">EXAMPLES</span></span>

### <span data-ttu-id="19a91-118">Exemplo 1: criar um contexto especificando um nome e uma chave de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="19a91-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="19a91-119">Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="19a91-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="19a91-120">Exemplo 2: criar um contexto especificando uma cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="19a91-120">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="19a91-121">Esse comando cria um contexto com base na cadeia de conexão especificada para a conta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="19a91-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="19a91-122">Exemplo 3: criar um contexto para uma conta de armazenamento anônimo</span><span class="sxs-lookup"><span data-stu-id="19a91-122">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="19a91-123">Esse comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="19a91-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="19a91-124">O comando especifica HTTP como um protocolo de conexão.</span><span class="sxs-lookup"><span data-stu-id="19a91-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="19a91-125">Exemplo 4: criar um contexto usando a conta de armazenamento de desenvolvimento local</span><span class="sxs-lookup"><span data-stu-id="19a91-125">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="19a91-126">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="19a91-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="19a91-127">O comando especifica o parâmetro *local* .</span><span class="sxs-lookup"><span data-stu-id="19a91-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="19a91-128">Exemplo 5: obter o contêiner para a conta de armazenamento do desenvolvedor local</span><span class="sxs-lookup"><span data-stu-id="19a91-128">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="19a91-129">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, passa o novo contexto para o cmdlet **Get-AzStorageContainer** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="19a91-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="19a91-130">O comando obtém o contêiner de armazenamento do Azure para a conta de armazenamento do desenvolvedor local.</span><span class="sxs-lookup"><span data-stu-id="19a91-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="19a91-131">Exemplo 6: obter vários contêineres</span><span class="sxs-lookup"><span data-stu-id="19a91-131">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="19a91-132">O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, armazena esse contexto na variável $Context 01.</span><span class="sxs-lookup"><span data-stu-id="19a91-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="19a91-133">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e, em seguida, armazena esse contexto na variável $Context 02.</span><span class="sxs-lookup"><span data-stu-id="19a91-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="19a91-134">O comando final Obtém os contêineres para os contextos armazenados em $Context 01 e $Context 02 usando **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="19a91-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="19a91-135">Exemplo 7: criar um contexto com um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="19a91-135">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="19a91-136">Esse comando cria um contexto de armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="19a91-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="19a91-137">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="19a91-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="19a91-138">Exemplo 8: criar um contexto com um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="19a91-138">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="19a91-139">Esse comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="19a91-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="19a91-140">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="19a91-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="19a91-141">Exemplo 9: criar um contexto usando um token SAS</span><span class="sxs-lookup"><span data-stu-id="19a91-141">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="19a91-142">O primeiro comando gera um token SAS usando o cmdlet **New-AzStorageContainerSASToken** para o contêiner chamado ContosoMain e, em seguida, armazena esse token na variável $SasToken.</span><span class="sxs-lookup"><span data-stu-id="19a91-142">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="19a91-143">Esse token é para permissões de leitura, adição, atualização e exclusão.</span><span class="sxs-lookup"><span data-stu-id="19a91-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="19a91-144">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e, em seguida, armazena esse contexto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="19a91-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="19a91-145">O comando final lista todos os BLOBs associados ao contêiner nomeado ContosoMain usando o contexto armazenado em $Context.</span><span class="sxs-lookup"><span data-stu-id="19a91-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="19a91-146">Exemplo 10: criar um contexto usando a autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="19a91-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="19a91-147">Esse comando cria um contexto usando a autenticação OAuth.</span><span class="sxs-lookup"><span data-stu-id="19a91-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="19a91-148">OS</span><span class="sxs-lookup"><span data-stu-id="19a91-148">PARAMETERS</span></span>

### <span data-ttu-id="19a91-149">-Anônimo</span><span class="sxs-lookup"><span data-stu-id="19a91-149">-Anonymous</span></span>
<span data-ttu-id="19a91-150">Indica que esse cmdlet cria um contexto de armazenamento do Azure para logon anônimo.</span><span class="sxs-lookup"><span data-stu-id="19a91-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="19a91-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="19a91-151">-ConnectionString</span></span>
<span data-ttu-id="19a91-152">Especifica uma cadeia de conexão para o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="19a91-153">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="19a91-153">-Endpoint</span></span>
<span data-ttu-id="19a91-154">Especifica o ponto de extremidade para o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-154">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="19a91-155">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="19a91-155">-Environment</span></span>
<span data-ttu-id="19a91-156">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="19a91-157">Os valores aceitáveis para esse parâmetro são: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="19a91-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="19a91-158">Para obter mais informações, digite `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="19a91-158">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="19a91-159">-Local</span><span class="sxs-lookup"><span data-stu-id="19a91-159">-Local</span></span>
<span data-ttu-id="19a91-160">Indica que esse cmdlet cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="19a91-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="19a91-161">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="19a91-161">-Protocol</span></span>
<span data-ttu-id="19a91-162">Protocolo de transferência (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="19a91-162">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="19a91-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="19a91-163">-SasToken</span></span>
<span data-ttu-id="19a91-164">Especifica um token de assinatura de acesso compartilhado (SAS) para o contexto.</span><span class="sxs-lookup"><span data-stu-id="19a91-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="19a91-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="19a91-165">-StorageAccountKey</span></span>
<span data-ttu-id="19a91-166">Especifica uma chave de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="19a91-167">Esse cmdlet cria um contexto para a chave que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="19a91-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="19a91-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19a91-168">-StorageAccountName</span></span>
<span data-ttu-id="19a91-169">Especifica um nome de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a91-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="19a91-170">Esse cmdlet cria um contexto para a conta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="19a91-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="19a91-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="19a91-171">-UseConnectedAccount</span></span>
<span data-ttu-id="19a91-172">Indica que esse cmdlet cria um contexto de armazenamento do Azure com Autenticação OAuth.</span><span class="sxs-lookup"><span data-stu-id="19a91-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="19a91-173">O cmdlet usará a autenticação OAuth por padrão, quando outros anthentication não forem especificados.</span><span class="sxs-lookup"><span data-stu-id="19a91-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

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

### <span data-ttu-id="19a91-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a91-174">CommonParameters</span></span>
<span data-ttu-id="19a91-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19a91-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a91-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19a91-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a91-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19a91-177">INPUTS</span></span>

### <span data-ttu-id="19a91-178">System. String</span><span class="sxs-lookup"><span data-stu-id="19a91-178">System.String</span></span>

## <span data-ttu-id="19a91-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19a91-179">OUTPUTS</span></span>

### <span data-ttu-id="19a91-180">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="19a91-180">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="19a91-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19a91-181">NOTES</span></span>

## <span data-ttu-id="19a91-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19a91-182">RELATED LINKS</span></span>

[<span data-ttu-id="19a91-183">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="19a91-183">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="19a91-184">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="19a91-184">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


