---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: ff97ccbe74d7f9a0005d2ad4d8b2cd44ad0da7e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774201"
---
# <span data-ttu-id="e3aad-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e3aad-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="e3aad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3aad-102">SYNOPSIS</span></span>
<span data-ttu-id="e3aad-103">Gera um token SAS para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3aad-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="e3aad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3aad-104">SYNTAX</span></span>

### <span data-ttu-id="e3aad-105">BlobNameWithPermission (padrão)</span><span class="sxs-lookup"><span data-stu-id="e3aad-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3aad-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e3aad-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3aad-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="e3aad-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3aad-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e3aad-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3aad-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3aad-109">DESCRIPTION</span></span>
<span data-ttu-id="e3aad-110">O cmdlet **New-AzStorageBlobSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3aad-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="e3aad-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3aad-111">EXAMPLES</span></span>

### <span data-ttu-id="e3aad-112">Exemplo 1: gerar um token SAS de blob com permissão completa de BLOB</span><span class="sxs-lookup"><span data-stu-id="e3aad-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="e3aad-113">Este exemplo gera um token SAS de blob com permissão de blob completo.</span><span class="sxs-lookup"><span data-stu-id="e3aad-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="e3aad-114">Exemplo 2: gerar um token SAS de blob com tempo de vida</span><span class="sxs-lookup"><span data-stu-id="e3aad-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e3aad-115">Este exemplo gera um token SAS de blob com tempo de vida útil.</span><span class="sxs-lookup"><span data-stu-id="e3aad-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="e3aad-116">OS</span><span class="sxs-lookup"><span data-stu-id="e3aad-116">PARAMETERS</span></span>

### <span data-ttu-id="e3aad-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="e3aad-117">-Blob</span></span>
<span data-ttu-id="e3aad-118">Especifica o nome do blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3aad-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="e3aad-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e3aad-119">-CloudBlob</span></span>
<span data-ttu-id="e3aad-120">Especifica o objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="e3aad-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="e3aad-121">Para obter um objeto **CloudBlob** , use o cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="e3aad-121">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="e3aad-122">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="e3aad-122">-Container</span></span>
<span data-ttu-id="e3aad-123">Especifica o nome do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3aad-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="e3aad-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e3aad-124">-Context</span></span>
<span data-ttu-id="e3aad-125">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3aad-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="e3aad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3aad-126">-DefaultProfile</span></span>
<span data-ttu-id="e3aad-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3aad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3aad-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e3aad-128">-ExpiryTime</span></span>
<span data-ttu-id="e3aad-129">Especifica quando a assinatura de acesso compartilhado expira.</span><span class="sxs-lookup"><span data-stu-id="e3aad-129">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="e3aad-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e3aad-130">-FullUri</span></span>
<span data-ttu-id="e3aad-131">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e3aad-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e3aad-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e3aad-132">-IPAddressOrRange</span></span>
<span data-ttu-id="e3aad-133">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="e3aad-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e3aad-134">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="e3aad-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="e3aad-135">-Permissão</span><span class="sxs-lookup"><span data-stu-id="e3aad-135">-Permission</span></span>
<span data-ttu-id="e3aad-136">Especifica as permissões para um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3aad-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="e3aad-137">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="e3aad-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="e3aad-138">-Política</span><span class="sxs-lookup"><span data-stu-id="e3aad-138">-Policy</span></span>
<span data-ttu-id="e3aad-139">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3aad-139">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="e3aad-140">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e3aad-140">-Protocol</span></span>
<span data-ttu-id="e3aad-141">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e3aad-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e3aad-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e3aad-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e3aad-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e3aad-143">HttpsOnly</span></span>
* <span data-ttu-id="e3aad-144">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e3aad-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e3aad-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e3aad-145">-StartTime</span></span>
<span data-ttu-id="e3aad-146">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="e3aad-146">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e3aad-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3aad-147">CommonParameters</span></span>
<span data-ttu-id="e3aad-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3aad-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3aad-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3aad-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3aad-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3aad-150">INPUTS</span></span>

### <span data-ttu-id="e3aad-151">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e3aad-151">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e3aad-152">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3aad-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e3aad-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3aad-153">OUTPUTS</span></span>

### <span data-ttu-id="e3aad-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e3aad-154">System.String</span></span>

## <span data-ttu-id="e3aad-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3aad-155">NOTES</span></span>

## <span data-ttu-id="e3aad-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3aad-156">RELATED LINKS</span></span>

[<span data-ttu-id="e3aad-157">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e3aad-157">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e3aad-158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e3aad-158">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
