---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426134"
---
# <span data-ttu-id="add54-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="add54-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="add54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="add54-102">SYNOPSIS</span></span>
<span data-ttu-id="add54-103">Gera um token SAS para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="add54-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="add54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="add54-104">SYNTAX</span></span>

### <span data-ttu-id="add54-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="add54-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="add54-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="add54-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="add54-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="add54-107">DESCRIPTION</span></span>
<span data-ttu-id="add54-108">O cmdlet **New-AzureStorageContainerSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="add54-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="add54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="add54-109">EXAMPLES</span></span>

### <span data-ttu-id="add54-110">Exemplo 1: gerar um token SAS de contêiner com permissão de contêiner completo</span><span class="sxs-lookup"><span data-stu-id="add54-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="add54-111">Este exemplo gera um token SAS de contêiner com permissão de contêiner completo.</span><span class="sxs-lookup"><span data-stu-id="add54-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="add54-112">Exemplo 2: gerar o token SAS de contêiner múltiplo por pipeline</span><span class="sxs-lookup"><span data-stu-id="add54-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="add54-113">Este exemplo gera vários tokens de SAS de contêiner usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="add54-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="add54-114">Exemplo 3: gerar token SAS de contêiner com política de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="add54-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="add54-115">Este exemplo gera um token SAS de contêiner com política de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="add54-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="add54-116">OS</span><span class="sxs-lookup"><span data-stu-id="add54-116">PARAMETERS</span></span>

### <span data-ttu-id="add54-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="add54-117">-Context</span></span>
<span data-ttu-id="add54-118">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="add54-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="add54-119">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="add54-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="add54-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="add54-120">-ExpiryTime</span></span>
<span data-ttu-id="add54-121">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="add54-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="add54-122">Se o usuário definir a hora de início, mas não a hora de vencimento, o tempo de expiração será definido como a hora de início mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="add54-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="add54-123">Se nem a hora de início nem a hora de vencimento forem especificadas, o tempo de expiração será definido como a hora atual mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="add54-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="add54-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="add54-124">-FullUri</span></span>
<span data-ttu-id="add54-125">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="add54-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="add54-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="add54-126">-IPAddressOrRange</span></span>
<span data-ttu-id="add54-127">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="add54-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="add54-128">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="add54-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="add54-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="add54-129">-Name</span></span>
<span data-ttu-id="add54-130">Especifica um nome de contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="add54-130">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="add54-131">-Permissão</span><span class="sxs-lookup"><span data-stu-id="add54-131">-Permission</span></span>
<span data-ttu-id="add54-132">Especifica as permissões para um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="add54-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="add54-133">-Política</span><span class="sxs-lookup"><span data-stu-id="add54-133">-Policy</span></span>
<span data-ttu-id="add54-134">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="add54-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="add54-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="add54-135">-Protocol</span></span>
<span data-ttu-id="add54-136">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="add54-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="add54-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="add54-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="add54-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="add54-138">HttpsOnly</span></span>
* <span data-ttu-id="add54-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="add54-139">HttpsOrHttp</span></span>

<span data-ttu-id="add54-140">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="add54-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="add54-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="add54-141">-StartTime</span></span>
<span data-ttu-id="add54-142">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="add54-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="add54-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add54-143">CommonParameters</span></span>
<span data-ttu-id="add54-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add54-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add54-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add54-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add54-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="add54-146">INPUTS</span></span>

## <span data-ttu-id="add54-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="add54-147">OUTPUTS</span></span>

## <span data-ttu-id="add54-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="add54-148">NOTES</span></span>

## <span data-ttu-id="add54-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="add54-149">RELATED LINKS</span></span>

[<span data-ttu-id="add54-150">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="add54-150">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)