---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264624"
---
# <span data-ttu-id="c490e-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c490e-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="c490e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c490e-102">SYNOPSIS</span></span>
<span data-ttu-id="c490e-103">Gera um token SAS para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c490e-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="c490e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c490e-104">SYNTAX</span></span>

### <span data-ttu-id="c490e-105">BlobNameWithPermission (padrão)</span><span class="sxs-lookup"><span data-stu-id="c490e-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c490e-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="c490e-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c490e-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="c490e-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c490e-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="c490e-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c490e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c490e-109">DESCRIPTION</span></span>
<span data-ttu-id="c490e-110">O cmdlet **New-AzStorageBlobSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c490e-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="c490e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c490e-111">EXAMPLES</span></span>

### <span data-ttu-id="c490e-112">Exemplo 1: gerar um token SAS de blob com permissão completa de BLOB</span><span class="sxs-lookup"><span data-stu-id="c490e-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="c490e-113">Este exemplo gera um token SAS de blob com permissão de blob completo.</span><span class="sxs-lookup"><span data-stu-id="c490e-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="c490e-114">Exemplo 2: gerar um token SAS de blob com tempo de vida</span><span class="sxs-lookup"><span data-stu-id="c490e-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="c490e-115">Este exemplo gera um token SAS de blob com tempo de vida útil.</span><span class="sxs-lookup"><span data-stu-id="c490e-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="c490e-116">Exemplo 3: gerar um token de identidade de usuário SAS com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="c490e-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="c490e-117">Este exemplo gera um token SAS de blob de identidade do usuário com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="c490e-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="c490e-118">OS</span><span class="sxs-lookup"><span data-stu-id="c490e-118">PARAMETERS</span></span>

### <span data-ttu-id="c490e-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="c490e-119">-Blob</span></span>
<span data-ttu-id="c490e-120">Especifica o nome do blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c490e-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="c490e-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="c490e-121">-BlobBaseClient</span></span>
<span data-ttu-id="c490e-122">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="c490e-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c490e-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c490e-123">-CloudBlob</span></span>
<span data-ttu-id="c490e-124">Especifica o objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="c490e-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="c490e-125">Para obter um objeto **CloudBlob** , use o cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="c490e-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="c490e-126">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="c490e-126">-Container</span></span>
<span data-ttu-id="c490e-127">Especifica o nome do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c490e-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="c490e-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c490e-128">-Context</span></span>
<span data-ttu-id="c490e-129">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c490e-129">Specifies the storage context.</span></span>
<span data-ttu-id="c490e-130">Quando o contexto de armazenamento for baseado em Autenticação OAuth, o token SAS do blob de identidade do usuário será gerado.</span><span class="sxs-lookup"><span data-stu-id="c490e-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="c490e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c490e-131">-DefaultProfile</span></span>
<span data-ttu-id="c490e-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c490e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c490e-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c490e-133">-ExpiryTime</span></span>
<span data-ttu-id="c490e-134">Especifica quando a assinatura de acesso compartilhado expira.</span><span class="sxs-lookup"><span data-stu-id="c490e-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="c490e-135">Quando o contexto de armazenamento se baseia na autenticação OAuth, o tempo de expiração deve ser de 7 dias a partir da hora atual e não deve ser anterior à hora atual.</span><span class="sxs-lookup"><span data-stu-id="c490e-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="c490e-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c490e-136">-FullUri</span></span>
<span data-ttu-id="c490e-137">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="c490e-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c490e-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c490e-138">-IPAddressOrRange</span></span>
<span data-ttu-id="c490e-139">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c490e-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c490e-140">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="c490e-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="c490e-141">-Permissão</span><span class="sxs-lookup"><span data-stu-id="c490e-141">-Permission</span></span>
<span data-ttu-id="c490e-142">Especifica as permissões para um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c490e-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="c490e-143">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="c490e-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="c490e-144">-Política</span><span class="sxs-lookup"><span data-stu-id="c490e-144">-Policy</span></span>
<span data-ttu-id="c490e-145">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="c490e-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="c490e-146">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="c490e-146">-Protocol</span></span>
<span data-ttu-id="c490e-147">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c490e-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c490e-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c490e-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c490e-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c490e-149">HttpsOnly</span></span>
* <span data-ttu-id="c490e-150">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c490e-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c490e-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c490e-151">-StartTime</span></span>
<span data-ttu-id="c490e-152">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="c490e-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c490e-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c490e-153">-Confirm</span></span>
<span data-ttu-id="c490e-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c490e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c490e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c490e-155">-WhatIf</span></span>
<span data-ttu-id="c490e-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c490e-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c490e-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c490e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c490e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c490e-158">CommonParameters</span></span>
<span data-ttu-id="c490e-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c490e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c490e-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c490e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c490e-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c490e-161">INPUTS</span></span>

### <span data-ttu-id="c490e-162">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c490e-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c490e-163">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c490e-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c490e-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c490e-164">OUTPUTS</span></span>

### <span data-ttu-id="c490e-165">System. String</span><span class="sxs-lookup"><span data-stu-id="c490e-165">System.String</span></span>

## <span data-ttu-id="c490e-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c490e-166">NOTES</span></span>

## <span data-ttu-id="c490e-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c490e-167">RELATED LINKS</span></span>

[<span data-ttu-id="c490e-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c490e-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c490e-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c490e-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
