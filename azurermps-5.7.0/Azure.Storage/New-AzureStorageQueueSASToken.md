---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: da9394d4d255a4ac09c8de437ee72b9d399cda35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430562"
---
# <span data-ttu-id="81658-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="81658-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="81658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81658-102">SYNOPSIS</span></span>
<span data-ttu-id="81658-103">Gera um token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81658-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81658-104">SYNTAX</span></span>

### <span data-ttu-id="81658-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="81658-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="81658-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="81658-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="81658-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81658-107">DESCRIPTION</span></span>
<span data-ttu-id="81658-108">O cmdlet **New-AzureStorageQueueSASToken** gera token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81658-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="81658-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81658-109">EXAMPLES</span></span>

### <span data-ttu-id="81658-110">Exemplo 1: gerar um token SAS de fila com permissão completa</span><span class="sxs-lookup"><span data-stu-id="81658-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="81658-111">Este exemplo gera um token SAS de fila com permissão completa.</span><span class="sxs-lookup"><span data-stu-id="81658-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="81658-112">OS</span><span class="sxs-lookup"><span data-stu-id="81658-112">PARAMETERS</span></span>

### <span data-ttu-id="81658-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="81658-113">-Context</span></span>
<span data-ttu-id="81658-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81658-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="81658-115">Você pode criá-lo por New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81658-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="81658-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="81658-116">-ExpiryTime</span></span>
<span data-ttu-id="81658-117">Especifica quando a assinatura de acesso compartilhado não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="81658-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="81658-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="81658-118">-FullUri</span></span>
<span data-ttu-id="81658-119">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="81658-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="81658-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="81658-120">-IPAddressOrRange</span></span>
<span data-ttu-id="81658-121">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="81658-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="81658-122">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="81658-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="81658-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="81658-123">-Name</span></span>
<span data-ttu-id="81658-124">Especifica um nome de fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81658-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81658-125">-Permissão</span><span class="sxs-lookup"><span data-stu-id="81658-125">-Permission</span></span>
<span data-ttu-id="81658-126">Especifica as permissões para uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="81658-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="81658-127">-Política</span><span class="sxs-lookup"><span data-stu-id="81658-127">-Policy</span></span>
<span data-ttu-id="81658-128">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="81658-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="81658-129">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="81658-129">-Protocol</span></span>
<span data-ttu-id="81658-130">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="81658-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="81658-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="81658-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="81658-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="81658-132">HttpsOnly</span></span>
* <span data-ttu-id="81658-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="81658-133">HttpsOrHttp</span></span>

<span data-ttu-id="81658-134">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="81658-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="81658-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="81658-135">-StartTime</span></span>
<span data-ttu-id="81658-136">Especifica quando a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="81658-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="81658-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81658-137">CommonParameters</span></span>
<span data-ttu-id="81658-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81658-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81658-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81658-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81658-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81658-140">INPUTS</span></span>

### <span data-ttu-id="81658-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="81658-141">IStorageContext</span></span>

<span data-ttu-id="81658-142">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="81658-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="81658-143">String</span><span class="sxs-lookup"><span data-stu-id="81658-143">String</span></span>

<span data-ttu-id="81658-144">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="81658-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="81658-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81658-145">OUTPUTS</span></span>

### <span data-ttu-id="81658-146">System. String</span><span class="sxs-lookup"><span data-stu-id="81658-146">System.String</span></span>

## <span data-ttu-id="81658-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81658-147">NOTES</span></span>

## <span data-ttu-id="81658-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81658-148">RELATED LINKS</span></span>

