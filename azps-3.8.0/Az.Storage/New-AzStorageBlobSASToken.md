---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943137"
---
# <span data-ttu-id="cc6b3-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cc6b3-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="cc6b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6b3-103">Gera um token SAS para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="cc6b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc6b3-104">SYNTAX</span></span>

### <span data-ttu-id="cc6b3-105">BlobNameWithPermission (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc6b3-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc6b3-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="cc6b3-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc6b3-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="cc6b3-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc6b3-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="cc6b3-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc6b3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc6b3-109">DESCRIPTION</span></span>
<span data-ttu-id="cc6b3-110">O cmdlet **New-AzStorageBlobSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="cc6b3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc6b3-111">EXAMPLES</span></span>

### <span data-ttu-id="cc6b3-112">Exemplo 1: gerar um token SAS de blob com permissão completa de BLOB</span><span class="sxs-lookup"><span data-stu-id="cc6b3-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="cc6b3-113">Este exemplo gera um token SAS de blob com permissão de blob completo.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="cc6b3-114">Exemplo 2: gerar um token SAS de blob com tempo de vida</span><span class="sxs-lookup"><span data-stu-id="cc6b3-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="cc6b3-115">Este exemplo gera um token SAS de blob com tempo de vida útil.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="cc6b3-116">Exemplo 3: gerar um token de identidade de usuário SAS com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="cc6b3-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="cc6b3-117">Este exemplo gera um token SAS de blob de identidade do usuário com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="cc6b3-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="cc6b3-118">OS</span><span class="sxs-lookup"><span data-stu-id="cc6b3-118">PARAMETERS</span></span>

### <span data-ttu-id="cc6b3-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="cc6b3-119">-Blob</span></span>
<span data-ttu-id="cc6b3-120">Especifica o nome do blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-120">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc6b3-121">-CloudBlob</span></span>
<span data-ttu-id="cc6b3-122">Especifica o objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="cc6b3-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="cc6b3-123">Para obter um objeto **CloudBlob** , use o cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="cc6b3-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-124">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="cc6b3-124">-Container</span></span>
<span data-ttu-id="cc6b3-125">Especifica o nome do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-125">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-126">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cc6b3-126">-Context</span></span>
<span data-ttu-id="cc6b3-127">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-127">Specifies the storage context.</span></span>
<span data-ttu-id="cc6b3-128">Quando o contexto de armazenamento for baseado em Autenticação OAuth, o token SAS do blob de identidade do usuário será gerado.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="cc6b3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6b3-129">-DefaultProfile</span></span>
<span data-ttu-id="cc6b3-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc6b3-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cc6b3-131">-ExpiryTime</span></span>
<span data-ttu-id="cc6b3-132">Especifica quando a assinatura de acesso compartilhado expira.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="cc6b3-133">Quando o contexto de armazenamento se baseia na autenticação OAuth, o tempo de expiração deve ser de 7 dias a partir da hora atual e não deve ser anterior à hora atual.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="cc6b3-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="cc6b3-134">-FullUri</span></span>
<span data-ttu-id="cc6b3-135">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="cc6b3-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cc6b3-136">-IPAddressOrRange</span></span>
<span data-ttu-id="cc6b3-137">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="cc6b3-138">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="cc6b3-139">-Permissão</span><span class="sxs-lookup"><span data-stu-id="cc6b3-139">-Permission</span></span>
<span data-ttu-id="cc6b3-140">Especifica as permissões para um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="cc6b3-141">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="cc6b3-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-142">-Política</span><span class="sxs-lookup"><span data-stu-id="cc6b3-142">-Policy</span></span>
<span data-ttu-id="cc6b3-143">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-143">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-144">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="cc6b3-144">-Protocol</span></span>
<span data-ttu-id="cc6b3-145">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="cc6b3-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cc6b3-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="cc6b3-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="cc6b3-147">HttpsOnly</span></span>
* <span data-ttu-id="cc6b3-148">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="cc6b3-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cc6b3-149">-StartTime</span></span>
<span data-ttu-id="cc6b3-150">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="cc6b3-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc6b3-151">-Confirm</span></span>
<span data-ttu-id="cc6b3-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc6b3-153">-WhatIf</span></span>
<span data-ttu-id="cc6b3-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc6b3-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6b3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6b3-156">CommonParameters</span></span>
<span data-ttu-id="cc6b3-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6b3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6b3-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc6b3-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6b3-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc6b3-159">INPUTS</span></span>

### <span data-ttu-id="cc6b3-160">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="cc6b3-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="cc6b3-161">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc6b3-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cc6b3-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc6b3-162">OUTPUTS</span></span>

### <span data-ttu-id="cc6b3-163">System. String</span><span class="sxs-lookup"><span data-stu-id="cc6b3-163">System.String</span></span>

## <span data-ttu-id="cc6b3-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc6b3-164">NOTES</span></span>

## <span data-ttu-id="cc6b3-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc6b3-165">RELATED LINKS</span></span>

[<span data-ttu-id="cc6b3-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cc6b3-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="cc6b3-167">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cc6b3-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
