---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d7c7847a92c7bbb241046479c70d1dabb75ea685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427061"
---
# <span data-ttu-id="e0917-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e0917-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="e0917-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0917-102">SYNOPSIS</span></span>
<span data-ttu-id="e0917-103">Gera um token SAS para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0917-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0917-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0917-104">SYNTAX</span></span>

### <span data-ttu-id="e0917-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="e0917-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e0917-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="e0917-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e0917-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0917-107">DESCRIPTION</span></span>
<span data-ttu-id="e0917-108">O cmdlet **New-AzureStorageContainerSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0917-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="e0917-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0917-109">EXAMPLES</span></span>

### <span data-ttu-id="e0917-110">Exemplo 1: gerar um token SAS de contêiner com permissão de contêiner completo</span><span class="sxs-lookup"><span data-stu-id="e0917-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="e0917-111">Este exemplo gera um token SAS de contêiner com permissão de contêiner completo.</span><span class="sxs-lookup"><span data-stu-id="e0917-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="e0917-112">Exemplo 2: gerar o token SAS de contêiner múltiplo por pipeline</span><span class="sxs-lookup"><span data-stu-id="e0917-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="e0917-113">Este exemplo gera vários tokens de SAS de contêiner usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0917-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="e0917-114">Exemplo 3: gerar token SAS de contêiner com política de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="e0917-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="e0917-115">Este exemplo gera um token SAS de contêiner com política de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e0917-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="e0917-116">OS</span><span class="sxs-lookup"><span data-stu-id="e0917-116">PARAMETERS</span></span>

### <span data-ttu-id="e0917-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e0917-117">-Context</span></span>
<span data-ttu-id="e0917-118">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0917-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e0917-119">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e0917-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0917-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e0917-120">-ExpiryTime</span></span>
<span data-ttu-id="e0917-121">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="e0917-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="e0917-122">Se o usuário definir a hora de início, mas não a hora de vencimento, o tempo de expiração será definido como a hora de início mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="e0917-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="e0917-123">Se nem a hora de início nem a hora de vencimento forem especificadas, o tempo de expiração será definido como a hora atual mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="e0917-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="e0917-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e0917-124">-FullUri</span></span>
<span data-ttu-id="e0917-125">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e0917-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e0917-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e0917-126">-IPAddressOrRange</span></span>
<span data-ttu-id="e0917-127">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="e0917-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e0917-128">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="e0917-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="e0917-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0917-129">-Name</span></span>
<span data-ttu-id="e0917-130">Especifica um nome de contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0917-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0917-131">-Permissão</span><span class="sxs-lookup"><span data-stu-id="e0917-131">-Permission</span></span>
<span data-ttu-id="e0917-132">Especifica as permissões para um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e0917-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="e0917-133">-Política</span><span class="sxs-lookup"><span data-stu-id="e0917-133">-Policy</span></span>
<span data-ttu-id="e0917-134">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0917-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="e0917-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e0917-135">-Protocol</span></span>
<span data-ttu-id="e0917-136">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e0917-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e0917-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e0917-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e0917-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e0917-138">HttpsOnly</span></span>
* <span data-ttu-id="e0917-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e0917-139">HttpsOrHttp</span></span>

<span data-ttu-id="e0917-140">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e0917-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e0917-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e0917-141">-StartTime</span></span>
<span data-ttu-id="e0917-142">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="e0917-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e0917-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0917-143">CommonParameters</span></span>
<span data-ttu-id="e0917-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0917-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0917-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0917-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0917-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0917-146">INPUTS</span></span>

### <span data-ttu-id="e0917-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0917-147">IStorageContext</span></span>

<span data-ttu-id="e0917-148">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e0917-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e0917-149">String</span><span class="sxs-lookup"><span data-stu-id="e0917-149">String</span></span>

<span data-ttu-id="e0917-150">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e0917-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e0917-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0917-151">OUTPUTS</span></span>

### <span data-ttu-id="e0917-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e0917-152">System.String</span></span>

## <span data-ttu-id="e0917-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0917-153">NOTES</span></span>

## <span data-ttu-id="e0917-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0917-154">RELATED LINKS</span></span>

[<span data-ttu-id="e0917-155">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e0917-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
