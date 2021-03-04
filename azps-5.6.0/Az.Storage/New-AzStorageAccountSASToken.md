---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891978"
---
# <span data-ttu-id="20c3c-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="20c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="20c3c-103">Cria um token SAS no nível da conta.</span><span class="sxs-lookup"><span data-stu-id="20c3c-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="20c3c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20c3c-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c3c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="20c3c-106">O cmdlet **New-AzStorageSASToken** cria um token SAS (assinatura de acesso compartilhado) no nível da conta para uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="20c3c-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="20c3c-107">Você pode usar o token SAS para delegar permissões para vários serviços ou para delegar permissões para serviços não disponíveis com um token SAS de nível de objeto.</span><span class="sxs-lookup"><span data-stu-id="20c3c-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="20c3c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20c3c-108">EXAMPLES</span></span>

### <span data-ttu-id="20c3c-109">Exemplo 1: Criar um token SAS no nível da conta com permissão total</span><span class="sxs-lookup"><span data-stu-id="20c3c-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="20c3c-110">Este comando cria um token SAS no nível da conta com permissão total.</span><span class="sxs-lookup"><span data-stu-id="20c3c-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="20c3c-111">Exemplo 2: Criar um token SAS no nível da conta para um intervalo de endereços IP</span><span class="sxs-lookup"><span data-stu-id="20c3c-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="20c3c-112">Este comando cria um token SAS no nível da conta para solicitações somente HTTPS do intervalo especificado de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="20c3c-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="20c3c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20c3c-113">PARAMETERS</span></span>

### <span data-ttu-id="20c3c-114">-Context</span><span class="sxs-lookup"><span data-stu-id="20c3c-114">-Context</span></span>
<span data-ttu-id="20c3c-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="20c3c-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="20c3c-116">Você pode usar o cmdlet New-AzStorageContext para obter um **objeto AzureStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="20c3c-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20c3c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c3c-117">-DefaultProfile</span></span>
<span data-ttu-id="20c3c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20c3c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c3c-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="20c3c-119">-ExpiryTime</span></span>
<span data-ttu-id="20c3c-120">Especifica o momento em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="20c3c-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="20c3c-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="20c3c-121">-IPAddressOrRange</span></span>
<span data-ttu-id="20c3c-122">Especifica o endereço IP ou intervalo de endereços IP dos quais aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="20c3c-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="20c3c-123">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="20c3c-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="20c3c-124">-Permission</span><span class="sxs-lookup"><span data-stu-id="20c3c-124">-Permission</span></span>
<span data-ttu-id="20c3c-125">Especifica as permissões para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20c3c-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="20c3c-126">As permissões só serão válidas se corresponderem ao tipo de recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="20c3c-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="20c3c-127">É importante observar que esta é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="20c3c-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="20c3c-128">Para obter mais informações sobre valores de permissão aceitáveis, consulte Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="20c3c-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="20c3c-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="20c3c-129">-Protocol</span></span>
<span data-ttu-id="20c3c-130">Especifica o protocolo permitido para uma solicitação feita com o SAS da conta.</span><span class="sxs-lookup"><span data-stu-id="20c3c-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="20c3c-131">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20c3c-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20c3c-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="20c3c-132">HttpsOnly</span></span>
- <span data-ttu-id="20c3c-133">HttpsOrHttp O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="20c3c-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c3c-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="20c3c-134">-ResourceType</span></span>
<span data-ttu-id="20c3c-135">Especifica os tipos de recursos que estão disponíveis com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="20c3c-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="20c3c-136">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20c3c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20c3c-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20c3c-137">None</span></span>
- <span data-ttu-id="20c3c-138">Serviço</span><span class="sxs-lookup"><span data-stu-id="20c3c-138">Service</span></span>
- <span data-ttu-id="20c3c-139">Contêiner</span><span class="sxs-lookup"><span data-stu-id="20c3c-139">Container</span></span>
- <span data-ttu-id="20c3c-140">Objeto</span><span class="sxs-lookup"><span data-stu-id="20c3c-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c3c-141">-Service</span><span class="sxs-lookup"><span data-stu-id="20c3c-141">-Service</span></span>
<span data-ttu-id="20c3c-142">Especifica o serviço.</span><span class="sxs-lookup"><span data-stu-id="20c3c-142">Specifies the service.</span></span>
<span data-ttu-id="20c3c-143">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20c3c-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20c3c-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20c3c-144">None</span></span>
- <span data-ttu-id="20c3c-145">Blob</span><span class="sxs-lookup"><span data-stu-id="20c3c-145">Blob</span></span>
- <span data-ttu-id="20c3c-146">Arquivo</span><span class="sxs-lookup"><span data-stu-id="20c3c-146">File</span></span>
- <span data-ttu-id="20c3c-147">Fila</span><span class="sxs-lookup"><span data-stu-id="20c3c-147">Queue</span></span>
- <span data-ttu-id="20c3c-148">Tabela</span><span class="sxs-lookup"><span data-stu-id="20c3c-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c3c-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="20c3c-149">-StartTime</span></span>
<span data-ttu-id="20c3c-150">Especifica a hora, como um **objeto DateTime,** no qual o SAS se torna válido.</span><span class="sxs-lookup"><span data-stu-id="20c3c-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="20c3c-151">Para obter um **objeto DateTime,** use o Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20c3c-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="20c3c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c3c-152">CommonParameters</span></span>
<span data-ttu-id="20c3c-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c3c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c3c-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c3c-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c3c-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20c3c-155">INPUTS</span></span>

### <span data-ttu-id="20c3c-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20c3c-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="20c3c-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20c3c-157">OUTPUTS</span></span>

### <span data-ttu-id="20c3c-158">System.String</span><span class="sxs-lookup"><span data-stu-id="20c3c-158">System.String</span></span>

## <span data-ttu-id="20c3c-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="20c3c-159">NOTES</span></span>

## <span data-ttu-id="20c3c-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20c3c-160">RELATED LINKS</span></span>

[<span data-ttu-id="20c3c-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="20c3c-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="20c3c-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="20c3c-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="20c3c-165">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="20c3c-166">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="20c3c-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


