---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: 66c89b70b80cf56471e5d12aec975e4e568d5a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431510"
---
# <span data-ttu-id="048ec-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="048ec-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="048ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="048ec-102">SYNOPSIS</span></span>
<span data-ttu-id="048ec-103">Gera um token de assinatura de acesso compartilhado para um arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="048ec-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="048ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="048ec-104">SYNTAX</span></span>

### <span data-ttu-id="048ec-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="048ec-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="048ec-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="048ec-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="048ec-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="048ec-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="048ec-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="048ec-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="048ec-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="048ec-109">DESCRIPTION</span></span>
<span data-ttu-id="048ec-110">O cmdlet **New-AzureStorageFileSASToken** gera um token de assinatura de acesso compartilhado para um arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="048ec-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="048ec-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="048ec-111">EXAMPLES</span></span>

### <span data-ttu-id="048ec-112">Exemplo 1: gerar um token de assinatura de acesso compartilhado com permissões de arquivo completas</span><span class="sxs-lookup"><span data-stu-id="048ec-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="048ec-113">Esse comando gera um token de assinatura de acesso compartilhado que tem permissões completas para o arquivo chamado FilePath.</span><span class="sxs-lookup"><span data-stu-id="048ec-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="048ec-114">Exemplo 2: gerar um token de assinatura de acesso compartilhado que tenha um limite de tempo</span><span class="sxs-lookup"><span data-stu-id="048ec-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="048ec-115">O primeiro comando cria um objeto **DateTime** usando o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="048ec-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="048ec-116">O comando armazena a hora atual na variável $StartTime.</span><span class="sxs-lookup"><span data-stu-id="048ec-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="048ec-117">O segundo comando adiciona duas horas ao objeto no $StartTime e armazena o resultado na variável $EndTime.</span><span class="sxs-lookup"><span data-stu-id="048ec-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="048ec-118">Esse objeto é uma hora de duas horas no futuro.</span><span class="sxs-lookup"><span data-stu-id="048ec-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="048ec-119">O terceiro comando gera um token de assinatura de acesso compartilhado que tem as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="048ec-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="048ec-120">Esse token se torna válido no momento atual.</span><span class="sxs-lookup"><span data-stu-id="048ec-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="048ec-121">O token permanecerá válido até o tempo ser armazenado em $EndTime.</span><span class="sxs-lookup"><span data-stu-id="048ec-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="048ec-122">OS</span><span class="sxs-lookup"><span data-stu-id="048ec-122">PARAMETERS</span></span>

### <span data-ttu-id="048ec-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="048ec-123">-Context</span></span>
<span data-ttu-id="048ec-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="048ec-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="048ec-125">Para obter um contexto, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="048ec-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048ec-126">-DefaultProfile</span></span>
<span data-ttu-id="048ec-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="048ec-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="048ec-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="048ec-128">-ExpiryTime</span></span>
<span data-ttu-id="048ec-129">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="048ec-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="048ec-130">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="048ec-130">-File</span></span>
<span data-ttu-id="048ec-131">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="048ec-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="048ec-132">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="048ec-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="048ec-133">-FullUri</span></span>
<span data-ttu-id="048ec-134">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="048ec-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="048ec-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="048ec-135">-IPAddressOrRange</span></span>
<span data-ttu-id="048ec-136">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="048ec-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="048ec-137">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="048ec-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="048ec-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="048ec-138">-Path</span></span>
<span data-ttu-id="048ec-139">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="048ec-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-140">-Permissão</span><span class="sxs-lookup"><span data-stu-id="048ec-140">-Permission</span></span>
<span data-ttu-id="048ec-141">Especifica as permissões para um arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="048ec-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="048ec-142">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="048ec-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-143">-Política</span><span class="sxs-lookup"><span data-stu-id="048ec-143">-Policy</span></span>
<span data-ttu-id="048ec-144">Especifica a política de acesso armazenada para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="048ec-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-145">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="048ec-145">-Protocol</span></span>
<span data-ttu-id="048ec-146">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="048ec-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="048ec-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="048ec-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="048ec-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="048ec-148">HttpsOnly</span></span>
* <span data-ttu-id="048ec-149">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="048ec-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="048ec-150">-ShareName</span></span>
<span data-ttu-id="048ec-151">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="048ec-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="048ec-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="048ec-152">-StartTime</span></span>
<span data-ttu-id="048ec-153">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="048ec-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="048ec-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048ec-154">CommonParameters</span></span>
<span data-ttu-id="048ec-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048ec-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048ec-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048ec-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048ec-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="048ec-157">INPUTS</span></span>

### <span data-ttu-id="048ec-158">System. String</span><span class="sxs-lookup"><span data-stu-id="048ec-158">System.String</span></span>

### <span data-ttu-id="048ec-159">Microsoft. WindowsAzure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="048ec-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="048ec-160">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="048ec-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>
<span data-ttu-id="048ec-161">Parâmetros: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="048ec-161">Parameters: Context (ByValue)</span></span>

## <span data-ttu-id="048ec-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="048ec-162">OUTPUTS</span></span>

### <span data-ttu-id="048ec-163">System. String</span><span class="sxs-lookup"><span data-stu-id="048ec-163">System.String</span></span>

## <span data-ttu-id="048ec-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="048ec-164">NOTES</span></span>

## <span data-ttu-id="048ec-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="048ec-165">RELATED LINKS</span></span>

[<span data-ttu-id="048ec-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="048ec-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="048ec-167">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="048ec-167">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)