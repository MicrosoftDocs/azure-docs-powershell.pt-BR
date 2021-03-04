---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 65a90f703f142a01429fb215bd5c66bef74bb4c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892689"
---
# <span data-ttu-id="b4210-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="b4210-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="b4210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4210-102">SYNOPSIS</span></span>
<span data-ttu-id="b4210-103">Gera um token SAS para uma tabela de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4210-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="b4210-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4210-104">SYNTAX</span></span>

### <span data-ttu-id="b4210-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b4210-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4210-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b4210-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4210-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4210-107">DESCRIPTION</span></span>
<span data-ttu-id="b4210-108">O cmdlet **New-AzStorageTableSASToken** gera um token SAS (Assinatura de Acesso Compartilhado) para uma tabela de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4210-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="b4210-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4210-109">EXAMPLES</span></span>

### <span data-ttu-id="b4210-110">Exemplo 1: Gerar um token SAS que tenha permissões completas para uma tabela</span><span class="sxs-lookup"><span data-stu-id="b4210-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="b4210-111">Este comando gera um token SAS com permissões completas para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="b4210-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="b4210-112">Esse token é para permissões de leitura, adicionar, atualizar e excluir.</span><span class="sxs-lookup"><span data-stu-id="b4210-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="b4210-113">Exemplo 2: Gerar um token SAS para um intervalo de partições</span><span class="sxs-lookup"><span data-stu-id="b4210-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="b4210-114">Este comando gera e token SAS com permissões completas para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="b4210-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="b4210-115">O comando limita o token ao intervalo especificado pelos *parâmetros StartPartitionKey* e *EndPartitionKey.*</span><span class="sxs-lookup"><span data-stu-id="b4210-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="b4210-116">Exemplo 3: Gerar um token SAS que tenha uma política de acesso armazenada para uma tabela</span><span class="sxs-lookup"><span data-stu-id="b4210-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="b4210-117">Esse comando gera um token SAS para a tabela chamada ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="b4210-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="b4210-118">O comando especifica a política de acesso armazenada chamada ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="b4210-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="b4210-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4210-119">PARAMETERS</span></span>

### <span data-ttu-id="b4210-120">-Context</span><span class="sxs-lookup"><span data-stu-id="b4210-120">-Context</span></span>
<span data-ttu-id="b4210-121">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4210-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b4210-122">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4210-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b4210-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4210-123">-DefaultProfile</span></span>
<span data-ttu-id="b4210-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4210-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4210-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="b4210-125">-EndPartitionKey</span></span>
<span data-ttu-id="b4210-126">Especifica a chave de partição do final do intervalo para o token que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="b4210-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="b4210-127">-EndRowKey</span></span>
<span data-ttu-id="b4210-128">Especifica a chave de linha para o final do intervalo para o token que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="b4210-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b4210-129">-ExpiryTime</span></span>
<span data-ttu-id="b4210-130">Especifica quando o token SAS expira.</span><span class="sxs-lookup"><span data-stu-id="b4210-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="b4210-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b4210-131">-FullUri</span></span>
<span data-ttu-id="b4210-132">Indica que esse cmdlet retorna o URI de fila completa com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="b4210-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="b4210-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b4210-133">-IPAddressOrRange</span></span>
<span data-ttu-id="b4210-134">Especifica o endereço IP ou intervalo de endereços IP dos quais aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b4210-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b4210-135">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="b4210-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="b4210-136">-Name</span><span class="sxs-lookup"><span data-stu-id="b4210-136">-Name</span></span>
<span data-ttu-id="b4210-137">Especifica o nome de uma tabela de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4210-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="b4210-138">Este cmdlet cria um token SAS para a tabela especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b4210-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-139">-Permission</span><span class="sxs-lookup"><span data-stu-id="b4210-139">-Permission</span></span>
<span data-ttu-id="b4210-140">Especifica permissões para uma tabela de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4210-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="b4210-141">É importante observar que esta é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="b4210-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="b4210-142">-Policy</span></span>
<span data-ttu-id="b4210-143">Especifica uma política de acesso armazenada, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="b4210-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b4210-144">-Protocol</span></span>
<span data-ttu-id="b4210-145">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4210-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b4210-146">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b4210-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b4210-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b4210-147">HttpsOnly</span></span>
* <span data-ttu-id="b4210-148">HttpsOrHttp O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="b4210-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="b4210-149">-StartPartitionKey</span></span>
<span data-ttu-id="b4210-150">Especifica a chave de partição do início do intervalo para o token que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="b4210-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="b4210-151">-StartRowKey</span></span>
<span data-ttu-id="b4210-152">Especifica a chave de linha para o início do intervalo para o token que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="b4210-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4210-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b4210-153">-StartTime</span></span>
<span data-ttu-id="b4210-154">Especifica quando o token SAS se torna válido.</span><span class="sxs-lookup"><span data-stu-id="b4210-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="b4210-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4210-155">CommonParameters</span></span>
<span data-ttu-id="b4210-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4210-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4210-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4210-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4210-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4210-158">INPUTS</span></span>

### <span data-ttu-id="b4210-159">System.String</span><span class="sxs-lookup"><span data-stu-id="b4210-159">System.String</span></span>

### <span data-ttu-id="b4210-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4210-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b4210-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4210-161">OUTPUTS</span></span>

### <span data-ttu-id="b4210-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b4210-162">System.String</span></span>

## <span data-ttu-id="b4210-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4210-163">NOTES</span></span>

## <span data-ttu-id="b4210-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4210-164">RELATED LINKS</span></span>

[<span data-ttu-id="b4210-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4210-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
