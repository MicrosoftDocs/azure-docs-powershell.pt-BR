---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 052eae9a995aafe9d5d966ae5a17aae31a0fc0fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611019"
---
# <span data-ttu-id="1fe46-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1fe46-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="1fe46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fe46-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe46-103">Gera um token de assinatura de acesso compartilhado para um arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fe46-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fe46-104">SYNTAX</span></span>

### <span data-ttu-id="1fe46-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="1fe46-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1fe46-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1fe46-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1fe46-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="1fe46-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="1fe46-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1fe46-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="1fe46-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fe46-109">DESCRIPTION</span></span>
<span data-ttu-id="1fe46-110">O cmdlet **New-AzureStorageFileSASToken** gera um token de assinatura de acesso compartilhado para um arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe46-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="1fe46-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fe46-111">EXAMPLES</span></span>

### <span data-ttu-id="1fe46-112">Exemplo 1: gerar um token de assinatura de acesso compartilhado com permissões de arquivo completas</span><span class="sxs-lookup"><span data-stu-id="1fe46-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="1fe46-113">Esse comando gera um token de assinatura de acesso compartilhado que tem permissões completas para o arquivo chamado FilePath.</span><span class="sxs-lookup"><span data-stu-id="1fe46-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="1fe46-114">Exemplo 2: gerar um token de assinatura de acesso compartilhado que tenha um limite de tempo</span><span class="sxs-lookup"><span data-stu-id="1fe46-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="1fe46-115">O primeiro comando cria um objeto **DateTime** usando o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="1fe46-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="1fe46-116">O comando armazena a hora atual na variável $StartTime.</span><span class="sxs-lookup"><span data-stu-id="1fe46-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="1fe46-117">O segundo comando adiciona duas horas ao objeto no $StartTime e armazena o resultado na variável $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1fe46-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="1fe46-118">Esse objeto é uma hora de duas horas no futuro.</span><span class="sxs-lookup"><span data-stu-id="1fe46-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="1fe46-119">O terceiro comando gera um token de assinatura de acesso compartilhado que tem as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="1fe46-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="1fe46-120">Esse token se torna válido no momento atual.</span><span class="sxs-lookup"><span data-stu-id="1fe46-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="1fe46-121">O token permanecerá válido até o tempo ser armazenado em $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1fe46-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="1fe46-122">OS</span><span class="sxs-lookup"><span data-stu-id="1fe46-122">PARAMETERS</span></span>

### <span data-ttu-id="1fe46-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1fe46-123">-Context</span></span>
<span data-ttu-id="1fe46-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe46-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1fe46-125">Para obter um contexto, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1fe46-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe46-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1fe46-126">-ExpiryTime</span></span>
<span data-ttu-id="1fe46-127">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="1fe46-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="1fe46-128">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="1fe46-128">-File</span></span>
<span data-ttu-id="1fe46-129">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="1fe46-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1fe46-130">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="1fe46-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe46-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1fe46-131">-FullUri</span></span>
<span data-ttu-id="1fe46-132">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="1fe46-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="1fe46-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1fe46-133">-IPAddressOrRange</span></span>
<span data-ttu-id="1fe46-134">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="1fe46-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1fe46-135">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="1fe46-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="1fe46-136">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1fe46-136">-Path</span></span>
<span data-ttu-id="1fe46-137">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fe46-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe46-138">-Permissão</span><span class="sxs-lookup"><span data-stu-id="1fe46-138">-Permission</span></span>
<span data-ttu-id="1fe46-139">Especifica as permissões para um arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fe46-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe46-140">-Política</span><span class="sxs-lookup"><span data-stu-id="1fe46-140">-Policy</span></span>
<span data-ttu-id="1fe46-141">Especifica a política de acesso armazenada para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1fe46-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe46-142">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="1fe46-142">-Protocol</span></span>
<span data-ttu-id="1fe46-143">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1fe46-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1fe46-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1fe46-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1fe46-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1fe46-145">HttpsOnly</span></span>
* <span data-ttu-id="1fe46-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1fe46-146">HttpsOrHttp</span></span>

<span data-ttu-id="1fe46-147">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="1fe46-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="1fe46-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1fe46-148">-ShareName</span></span>
<span data-ttu-id="1fe46-149">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fe46-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe46-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1fe46-150">-StartTime</span></span>
<span data-ttu-id="1fe46-151">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="1fe46-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="1fe46-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe46-152">CommonParameters</span></span>
<span data-ttu-id="1fe46-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe46-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe46-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe46-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe46-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fe46-155">INPUTS</span></span>

### <span data-ttu-id="1fe46-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fe46-156">IStorageContext</span></span>

<span data-ttu-id="1fe46-157">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe46-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1fe46-158">Cloudfile</span><span class="sxs-lookup"><span data-stu-id="1fe46-158">CloudFile</span></span>

<span data-ttu-id="1fe46-159">O parâmetro ' file ' aceita o valor do tipo ' Cloudfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe46-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="1fe46-160">String</span><span class="sxs-lookup"><span data-stu-id="1fe46-160">String</span></span>

<span data-ttu-id="1fe46-161">O parâmetro ' path ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe46-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="1fe46-162">String</span><span class="sxs-lookup"><span data-stu-id="1fe46-162">String</span></span>

<span data-ttu-id="1fe46-163">O parâmetro ' ShareName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe46-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1fe46-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fe46-164">OUTPUTS</span></span>

### <span data-ttu-id="1fe46-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1fe46-165">System.String</span></span>

## <span data-ttu-id="1fe46-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fe46-166">NOTES</span></span>

## <span data-ttu-id="1fe46-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fe46-167">RELATED LINKS</span></span>

[<span data-ttu-id="1fe46-168">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1fe46-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1fe46-169">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1fe46-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
