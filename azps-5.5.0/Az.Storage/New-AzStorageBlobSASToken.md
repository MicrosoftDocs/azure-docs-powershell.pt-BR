---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116334"
---
# <span data-ttu-id="01066-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="01066-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="01066-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01066-102">SYNOPSIS</span></span>
<span data-ttu-id="01066-103">Gera um token SAS para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="01066-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="01066-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01066-104">SYNTAX</span></span>

### <span data-ttu-id="01066-105">BlobNameWithPermission (Padrão)</span><span class="sxs-lookup"><span data-stu-id="01066-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01066-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="01066-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01066-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="01066-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01066-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="01066-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01066-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="01066-109">DESCRIPTION</span></span>
<span data-ttu-id="01066-110">O cmdlet **New-AzStorageBtrucSASToken** gera um token SAS (Assinatura de Acesso Compartilhado) para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="01066-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="01066-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01066-111">EXAMPLES</span></span>

### <span data-ttu-id="01066-112">Exemplo 1: Gerar um token SAS de blob com permissão de blob completa</span><span class="sxs-lookup"><span data-stu-id="01066-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="01066-113">Este exemplo gera um token SAS de blob com permissão total de blob.</span><span class="sxs-lookup"><span data-stu-id="01066-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="01066-114">Exemplo 2: Gerar um token SAS de blob com tempo de vida útil</span><span class="sxs-lookup"><span data-stu-id="01066-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="01066-115">Este exemplo gera um token SAS blob com tempo de vida útil.</span><span class="sxs-lookup"><span data-stu-id="01066-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="01066-116">Exemplo 3: Gerar um token SAS de identidade de usuário com contexto de armazenamento com base na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="01066-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="01066-117">Este exemplo gera um token SAS de blob identidade de usuário com contexto de armazenamento com base na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="01066-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="01066-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01066-118">PARAMETERS</span></span>

### <span data-ttu-id="01066-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="01066-119">-Blob</span></span>
<span data-ttu-id="01066-120">Especifica o nome do blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="01066-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="01066-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="01066-121">-BlobBaseClient</span></span>
<span data-ttu-id="01066-122">Objeto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="01066-122">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="01066-123">-CloudBlab</span><span class="sxs-lookup"><span data-stu-id="01066-123">-CloudBlob</span></span>
<span data-ttu-id="01066-124">Especifica o objeto **CloudB ltd.**</span><span class="sxs-lookup"><span data-stu-id="01066-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="01066-125">Para obter um **objeto CloudBtruc,** use o cmdlet [Get-AzStorageB ltd.](./Get-AzStorageBlob.md)</span><span class="sxs-lookup"><span data-stu-id="01066-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="01066-126">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="01066-126">-Container</span></span>
<span data-ttu-id="01066-127">Especifica o nome do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="01066-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="01066-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="01066-128">-Context</span></span>
<span data-ttu-id="01066-129">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="01066-129">Specifies the storage context.</span></span>
<span data-ttu-id="01066-130">Quando o contexto de armazenamento é baseado na autenticação OAuth, gera um token SAS de blob identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="01066-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="01066-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01066-131">-DefaultProfile</span></span>
<span data-ttu-id="01066-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01066-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01066-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="01066-133">-ExpiryTime</span></span>
<span data-ttu-id="01066-134">Especifica quando a assinatura de acesso compartilhado expira.</span><span class="sxs-lookup"><span data-stu-id="01066-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="01066-135">Quando o contexto de armazenamento se baseia na autenticação OAuth, a hora de expiração deve ser em sete dias a partir da hora atual e não deve ser anterior à hora atual.</span><span class="sxs-lookup"><span data-stu-id="01066-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="01066-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="01066-136">-FullUri</span></span>
<span data-ttu-id="01066-137">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="01066-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="01066-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="01066-138">-IPAddressOrRange</span></span>
<span data-ttu-id="01066-139">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="01066-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="01066-140">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="01066-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="01066-141">-Permissão</span><span class="sxs-lookup"><span data-stu-id="01066-141">-Permission</span></span>
<span data-ttu-id="01066-142">Especifica as permissões para um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="01066-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="01066-143">É importante observar que esta é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="01066-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="01066-144">-Política</span><span class="sxs-lookup"><span data-stu-id="01066-144">-Policy</span></span>
<span data-ttu-id="01066-145">Especifica uma Política de Acesso Armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="01066-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="01066-146">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="01066-146">-Protocol</span></span>
<span data-ttu-id="01066-147">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="01066-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="01066-148">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="01066-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="01066-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="01066-149">HttpsOnly</span></span>
* <span data-ttu-id="01066-150">HttpsOrHttp O valor padrão é httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="01066-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="01066-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="01066-151">-StartTime</span></span>
<span data-ttu-id="01066-152">Especifica o momento em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="01066-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="01066-153">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="01066-153">-Confirm</span></span>
<span data-ttu-id="01066-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01066-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01066-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01066-155">-WhatIf</span></span>
<span data-ttu-id="01066-156">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="01066-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01066-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01066-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01066-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01066-158">CommonParameters</span></span>
<span data-ttu-id="01066-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01066-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01066-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01066-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01066-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="01066-161">INPUTS</span></span>

### <span data-ttu-id="01066-162">Microsoft.Azure.Storage.Blob.CloudBlab</span><span class="sxs-lookup"><span data-stu-id="01066-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="01066-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01066-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="01066-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="01066-164">OUTPUTS</span></span>

### <span data-ttu-id="01066-165">System.String</span><span class="sxs-lookup"><span data-stu-id="01066-165">System.String</span></span>

## <span data-ttu-id="01066-166">Notas</span><span class="sxs-lookup"><span data-stu-id="01066-166">NOTES</span></span>

## <span data-ttu-id="01066-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01066-167">RELATED LINKS</span></span>

[<span data-ttu-id="01066-168">Get-AzStorageB ltd</span><span class="sxs-lookup"><span data-stu-id="01066-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="01066-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="01066-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
