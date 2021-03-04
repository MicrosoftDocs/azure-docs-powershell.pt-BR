---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891963"
---
# <span data-ttu-id="321d4-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="321d4-101">New-AzStorageContext</span></span>

## <span data-ttu-id="321d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="321d4-102">SYNOPSIS</span></span>
<span data-ttu-id="321d4-103">Cria um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="321d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="321d4-104">SYNTAX</span></span>

### <span data-ttu-id="321d4-105">OAuthAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="321d4-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="321d4-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="321d4-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="321d4-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="321d4-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="321d4-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="321d4-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="321d4-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="321d4-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="321d4-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="321d4-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="321d4-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="321d4-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="321d4-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="321d4-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="321d4-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="321d4-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="321d4-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="321d4-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="321d4-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="321d4-115">DESCRIPTION</span></span>
<span data-ttu-id="321d4-116">O cmdlet **New-AzStorageContext** cria um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="321d4-117">A Autenticação padrão de um contexto de armazenamento é OAuth (Azure AD), se apenas o nome da conta de armazenamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="321d4-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="321d4-118">Consulte detalhes da autenticação do Serviço de Armazenamento em https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="321d4-118">See details of authentication of the Storage Service in https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="321d4-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="321d4-119">EXAMPLES</span></span>

### <span data-ttu-id="321d4-120">Exemplo 1: Criar um contexto especificando um nome de conta de armazenamento e uma chave</span><span class="sxs-lookup"><span data-stu-id="321d4-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="321d4-121">Este comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="321d4-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="321d4-122">Exemplo 2: Criar um contexto especificando uma cadeia de caracteres de conexão</span><span class="sxs-lookup"><span data-stu-id="321d4-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="321d4-123">Este comando cria um contexto com base na cadeia de caracteres de conexão especificada para a conta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="321d4-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="321d4-124">Exemplo 3: criar um contexto para uma conta de armazenamento anônimo</span><span class="sxs-lookup"><span data-stu-id="321d4-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="321d4-125">Este comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="321d4-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="321d4-126">O comando especifica HTTP como um protocolo de conexão.</span><span class="sxs-lookup"><span data-stu-id="321d4-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="321d4-127">Exemplo 4: Criar um contexto usando a conta de armazenamento de desenvolvimento local</span><span class="sxs-lookup"><span data-stu-id="321d4-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="321d4-128">Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="321d4-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="321d4-129">O comando especifica o *parâmetro Local.*</span><span class="sxs-lookup"><span data-stu-id="321d4-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="321d4-130">Exemplo 5: Obter o contêiner para a conta de armazenamento de desenvolvedor local</span><span class="sxs-lookup"><span data-stu-id="321d4-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="321d4-131">Este comando cria um contexto usando a conta de armazenamento de desenvolvimento local e passa o novo contexto para o cmdlet **Get-AzStorageContainer** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="321d4-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="321d4-132">O comando obtém o contêiner de Armazenamento do Azure para a conta de armazenamento do desenvolvedor local.</span><span class="sxs-lookup"><span data-stu-id="321d4-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="321d4-133">Exemplo 6: Obter vários contêineres</span><span class="sxs-lookup"><span data-stu-id="321d4-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="321d4-134">O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e armazena esse contexto na variável $Context 01.</span><span class="sxs-lookup"><span data-stu-id="321d4-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="321d4-135">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e armazena esse contexto na variável $Context 02.</span><span class="sxs-lookup"><span data-stu-id="321d4-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="321d4-136">O comando final obtém os contêineres dos contextos armazenados em $Context 01 e $Context 02 usando **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="321d4-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="321d4-137">Exemplo 7: Criar um contexto com um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="321d4-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="321d4-138">Este comando cria um contexto de Armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="321d4-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="321d4-139">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="321d4-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="321d4-140">Exemplo 8: Criar um contexto com um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="321d4-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="321d4-141">Este comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="321d4-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="321d4-142">O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="321d4-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="321d4-143">Exemplo 9: Criar um contexto usando um token SAS</span><span class="sxs-lookup"><span data-stu-id="321d4-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="321d4-144">O primeiro comando gera um token SAS usando o cmdlet **New-AzStorageContainerSASToken** para o contêiner chamado ContosoMain e armazena esse token na variável $SasToken.</span><span class="sxs-lookup"><span data-stu-id="321d4-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="321d4-145">Esse token é para permissões de leitura, adicionar, atualizar e excluir.</span><span class="sxs-lookup"><span data-stu-id="321d4-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="321d4-146">O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e armazena esse contexto na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="321d4-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="321d4-147">O comando final lista todos os blobs associados ao contêiner chamado ContosoMain usando o contexto armazenado $Context.</span><span class="sxs-lookup"><span data-stu-id="321d4-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="321d4-148">Exemplo 10: Criar um contexto usando a Autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="321d4-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="321d4-149">Este comando cria um contexto usando a Autenticação OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="321d4-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="321d4-150">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="321d4-150">PARAMETERS</span></span>

### <span data-ttu-id="321d4-151">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="321d4-151">-Anonymous</span></span>
<span data-ttu-id="321d4-152">Indica que esse cmdlet cria um contexto de Armazenamento do Azure para logon anônimo.</span><span class="sxs-lookup"><span data-stu-id="321d4-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="321d4-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="321d4-153">-ConnectionString</span></span>
<span data-ttu-id="321d4-154">Especifica uma cadeia de caracteres de conexão para o contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="321d4-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="321d4-155">-Endpoint</span></span>
<span data-ttu-id="321d4-156">Especifica o ponto de extremidade para o contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="321d4-157">-Environment</span><span class="sxs-lookup"><span data-stu-id="321d4-157">-Environment</span></span>
<span data-ttu-id="321d4-158">Especifica o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="321d4-159">Os valores aceitáveis para este parâmetro são: AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="321d4-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="321d4-160">Para obter mais informações, digite `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="321d4-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="321d4-161">-Local</span><span class="sxs-lookup"><span data-stu-id="321d4-161">-Local</span></span>
<span data-ttu-id="321d4-162">Indica que esse cmdlet cria um contexto usando a conta de armazenamento de desenvolvimento local.</span><span class="sxs-lookup"><span data-stu-id="321d4-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="321d4-163">-Protocol</span><span class="sxs-lookup"><span data-stu-id="321d4-163">-Protocol</span></span>
<span data-ttu-id="321d4-164">Protocolo de Transferência (https/http).</span><span class="sxs-lookup"><span data-stu-id="321d4-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="321d4-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="321d4-165">-SasToken</span></span>
<span data-ttu-id="321d4-166">Especifica um token SAS (Assinatura de Acesso Compartilhado) para o contexto.</span><span class="sxs-lookup"><span data-stu-id="321d4-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="321d4-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="321d4-167">-StorageAccountKey</span></span>
<span data-ttu-id="321d4-168">Especifica uma chave de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="321d4-169">Este cmdlet cria um contexto para a chave especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="321d4-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="321d4-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="321d4-170">-StorageAccountName</span></span>
<span data-ttu-id="321d4-171">Especifica um nome de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="321d4-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="321d4-172">Este cmdlet cria um contexto para a conta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="321d4-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="321d4-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="321d4-173">-UseConnectedAccount</span></span>
<span data-ttu-id="321d4-174">Indica que esse cmdlet cria um contexto de Armazenamento do Azure com Autenticação OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="321d4-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="321d4-175">O cmdlet usará a Autenticação OAuth por padrão, quando outra autenticação não especificada.</span><span class="sxs-lookup"><span data-stu-id="321d4-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="321d4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321d4-176">CommonParameters</span></span>
<span data-ttu-id="321d4-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="321d4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321d4-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="321d4-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321d4-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="321d4-179">INPUTS</span></span>

### <span data-ttu-id="321d4-180">System.String</span><span class="sxs-lookup"><span data-stu-id="321d4-180">System.String</span></span>

## <span data-ttu-id="321d4-181">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="321d4-181">OUTPUTS</span></span>

### <span data-ttu-id="321d4-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="321d4-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="321d4-183">NOTES</span><span class="sxs-lookup"><span data-stu-id="321d4-183">NOTES</span></span>

## <span data-ttu-id="321d4-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="321d4-184">RELATED LINKS</span></span>

[<span data-ttu-id="321d4-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="321d4-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="321d4-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="321d4-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


