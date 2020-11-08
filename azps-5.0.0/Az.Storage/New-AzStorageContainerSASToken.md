---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117171"
---
# <span data-ttu-id="6d2a0-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6d2a0-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="6d2a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2a0-103">Gera um token SAS para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="6d2a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d2a0-104">SYNTAX</span></span>

### <span data-ttu-id="6d2a0-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="6d2a0-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d2a0-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="6d2a0-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d2a0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d2a0-107">DESCRIPTION</span></span>
<span data-ttu-id="6d2a0-108">O cmdlet **New-AzStorageContainerSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="6d2a0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d2a0-109">EXAMPLES</span></span>

### <span data-ttu-id="6d2a0-110">Exemplo 1: gerar um token SAS de contêiner com permissão de contêiner completo</span><span class="sxs-lookup"><span data-stu-id="6d2a0-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="6d2a0-111">Este exemplo gera um token SAS de contêiner com permissão de contêiner completo.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="6d2a0-112">Exemplo 2: gerar o token SAS de contêiner múltiplo por pipeline</span><span class="sxs-lookup"><span data-stu-id="6d2a0-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="6d2a0-113">Este exemplo gera vários tokens de SAS de contêiner usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="6d2a0-114">Exemplo 3: gerar token SAS de contêiner com política de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="6d2a0-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="6d2a0-115">Este exemplo gera um token SAS de contêiner com política de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="6d2a0-116">Exemplo 3: gerar um token SAS do contêiner de identidade do usuário com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="6d2a0-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="6d2a0-117">Este exemplo gera um token SAS do contêiner de identidade do usuário com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="6d2a0-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="6d2a0-118">OS</span><span class="sxs-lookup"><span data-stu-id="6d2a0-118">PARAMETERS</span></span>

### <span data-ttu-id="6d2a0-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6d2a0-119">-Context</span></span>
<span data-ttu-id="6d2a0-120">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6d2a0-121">Você pode criá-lo usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="6d2a0-122">Quando o contexto de armazenamento for baseado em Autenticação OAuth, o token SAS do contêiner de identidade do usuário será gerado.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="6d2a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2a0-123">-DefaultProfile</span></span>
<span data-ttu-id="6d2a0-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2a0-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6d2a0-125">-ExpiryTime</span></span>
<span data-ttu-id="6d2a0-126">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="6d2a0-127">Se o usuário definir a hora de início, mas não a hora de vencimento, o tempo de expiração será definido como a hora de início mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="6d2a0-128">Se nem a hora de início nem a hora de vencimento forem especificadas, o tempo de expiração será definido como a hora atual mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="6d2a0-129">Quando o contexto de armazenamento se baseia na autenticação OAuth, o tempo de expiração deve ser de 7 dias a partir da hora atual e não deve ser anterior à hora atual.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="6d2a0-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="6d2a0-130">-FullUri</span></span>
<span data-ttu-id="6d2a0-131">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="6d2a0-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6d2a0-132">-IPAddressOrRange</span></span>
<span data-ttu-id="6d2a0-133">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="6d2a0-134">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="6d2a0-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d2a0-135">-Name</span></span>
<span data-ttu-id="6d2a0-136">Especifica um nome de contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d2a0-137">-Permissão</span><span class="sxs-lookup"><span data-stu-id="6d2a0-137">-Permission</span></span>
<span data-ttu-id="6d2a0-138">Especifica as permissões para um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="6d2a0-139">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="6d2a0-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6d2a0-140">-Política</span><span class="sxs-lookup"><span data-stu-id="6d2a0-140">-Policy</span></span>
<span data-ttu-id="6d2a0-141">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="6d2a0-142">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6d2a0-142">-Protocol</span></span>
<span data-ttu-id="6d2a0-143">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="6d2a0-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="6d2a0-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="6d2a0-145">HttpsOnly</span></span>
* <span data-ttu-id="6d2a0-146">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="6d2a0-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6d2a0-147">-StartTime</span></span>
<span data-ttu-id="6d2a0-148">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="6d2a0-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d2a0-149">-Confirm</span></span>
<span data-ttu-id="6d2a0-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d2a0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d2a0-151">-WhatIf</span></span>
<span data-ttu-id="6d2a0-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d2a0-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d2a0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2a0-154">CommonParameters</span></span>
<span data-ttu-id="6d2a0-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2a0-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d2a0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2a0-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d2a0-157">INPUTS</span></span>

### <span data-ttu-id="6d2a0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6d2a0-158">System.String</span></span>

### <span data-ttu-id="6d2a0-159">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d2a0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6d2a0-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d2a0-160">OUTPUTS</span></span>

### <span data-ttu-id="6d2a0-161">System. String</span><span class="sxs-lookup"><span data-stu-id="6d2a0-161">System.String</span></span>

## <span data-ttu-id="6d2a0-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d2a0-162">NOTES</span></span>

## <span data-ttu-id="6d2a0-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d2a0-163">RELATED LINKS</span></span>

[<span data-ttu-id="6d2a0-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6d2a0-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
