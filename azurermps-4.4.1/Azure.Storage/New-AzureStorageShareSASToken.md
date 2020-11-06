---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 84f280bf5e3297796bb8b56e5a5d42e513b79e79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428026"
---
# <span data-ttu-id="a28df-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="a28df-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="a28df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a28df-102">SYNOPSIS</span></span>
<span data-ttu-id="a28df-103">Gerar token de assinatura de acesso compartilhado para compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a28df-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a28df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a28df-104">SYNTAX</span></span>

### <span data-ttu-id="a28df-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="a28df-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="a28df-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="a28df-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a28df-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a28df-107">DESCRIPTION</span></span>
<span data-ttu-id="a28df-108">O cmdlet **New-AzureStorageShareSASToken** gera um token de assinatura de acesso compartilhado para um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a28df-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="a28df-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a28df-109">EXAMPLES</span></span>

### <span data-ttu-id="a28df-110">Exemplo 1: gerar um token de assinatura de acesso compartilhado para um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="a28df-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="a28df-111">Esse comando cria um token de assinatura de acesso compartilhado para o compartilhamento chamado ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="a28df-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="a28df-112">Exemplo 2: gerar vários tokens de assinatura de acesso compartilhado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="a28df-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="a28df-113">Esse comando obtém todos os compartilhamentos de armazenamento correspondentes ao teste de prefixo.</span><span class="sxs-lookup"><span data-stu-id="a28df-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="a28df-114">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a28df-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a28df-115">O cmdlet atual cria um token de acesso compartilhado para cada compartilhamento de armazenamento que tenha as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="a28df-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="a28df-116">Exemplo 3: gerar um token de assinatura de acesso compartilhado que usa uma política de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="a28df-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="a28df-117">Esse comando cria um token de assinatura de acesso compartilhado para o compartilhamento de armazenamento chamado ContosoShare que tem a política chamada ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="a28df-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="a28df-118">OS</span><span class="sxs-lookup"><span data-stu-id="a28df-118">PARAMETERS</span></span>

### <span data-ttu-id="a28df-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a28df-119">-Context</span></span>
<span data-ttu-id="a28df-120">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a28df-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a28df-121">Para obter um contexto, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a28df-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a28df-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a28df-122">-ExpiryTime</span></span>
<span data-ttu-id="a28df-123">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="a28df-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="a28df-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="a28df-124">-FullUri</span></span>
<span data-ttu-id="a28df-125">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a28df-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="a28df-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a28df-126">-IPAddressOrRange</span></span>
<span data-ttu-id="a28df-127">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="a28df-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a28df-128">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="a28df-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="a28df-129">-Permissão</span><span class="sxs-lookup"><span data-stu-id="a28df-129">-Permission</span></span>
<span data-ttu-id="a28df-130">Especifica as permissões no token para acessar o compartilhamento e os arquivos no compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a28df-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

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

### <span data-ttu-id="a28df-131">-Política</span><span class="sxs-lookup"><span data-stu-id="a28df-131">-Policy</span></span>
<span data-ttu-id="a28df-132">Especifica a política de acesso armazenada para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a28df-132">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="a28df-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="a28df-133">-Protocol</span></span>
<span data-ttu-id="a28df-134">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a28df-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="a28df-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a28df-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="a28df-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a28df-136">HttpsOnly</span></span>
* <span data-ttu-id="a28df-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="a28df-137">HttpsOrHttp</span></span>

<span data-ttu-id="a28df-138">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="a28df-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="a28df-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a28df-139">-ShareName</span></span>
<span data-ttu-id="a28df-140">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a28df-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a28df-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a28df-141">-StartTime</span></span>
<span data-ttu-id="a28df-142">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="a28df-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="a28df-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28df-143">CommonParameters</span></span>
<span data-ttu-id="a28df-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28df-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28df-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28df-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28df-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a28df-146">INPUTS</span></span>

### <span data-ttu-id="a28df-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a28df-147">IStorageContext</span></span>

<span data-ttu-id="a28df-148">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a28df-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a28df-149">String</span><span class="sxs-lookup"><span data-stu-id="a28df-149">String</span></span>

<span data-ttu-id="a28df-150">O parâmetro ' ShareName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a28df-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a28df-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a28df-151">OUTPUTS</span></span>

### <span data-ttu-id="a28df-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a28df-152">System.String</span></span>

## <span data-ttu-id="a28df-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a28df-153">NOTES</span></span>
* <span data-ttu-id="a28df-154">Palavras-chave: comum, Azure, serviços, dados, armazenamento, BLOB, fila, tabela</span><span class="sxs-lookup"><span data-stu-id="a28df-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="a28df-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a28df-155">RELATED LINKS</span></span>

[<span data-ttu-id="a28df-156">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a28df-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a28df-157">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="a28df-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
