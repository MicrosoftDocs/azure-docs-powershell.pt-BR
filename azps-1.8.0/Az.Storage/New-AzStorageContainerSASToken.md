---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 88b9d395cca2e548e3c70d55267b7c1b3854a750
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598619"
---
# <span data-ttu-id="12b99-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="12b99-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="12b99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12b99-102">SYNOPSIS</span></span>
<span data-ttu-id="12b99-103">Gera um token SAS para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12b99-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="12b99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12b99-104">SYNTAX</span></span>

### <span data-ttu-id="12b99-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="12b99-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12b99-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="12b99-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12b99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12b99-107">DESCRIPTION</span></span>
<span data-ttu-id="12b99-108">O cmdlet **New-AzStorageContainerSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12b99-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="12b99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12b99-109">EXAMPLES</span></span>

### <span data-ttu-id="12b99-110">Exemplo 1: gerar um token SAS de contêiner com permissão de contêiner completo</span><span class="sxs-lookup"><span data-stu-id="12b99-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="12b99-111">Este exemplo gera um token SAS de contêiner com permissão de contêiner completo.</span><span class="sxs-lookup"><span data-stu-id="12b99-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="12b99-112">Exemplo 2: gerar o token SAS de contêiner múltiplo por pipeline</span><span class="sxs-lookup"><span data-stu-id="12b99-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="12b99-113">Este exemplo gera vários tokens de SAS de contêiner usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="12b99-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="12b99-114">Exemplo 3: gerar token SAS de contêiner com política de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="12b99-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="12b99-115">Este exemplo gera um token SAS de contêiner com política de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="12b99-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="12b99-116">OS</span><span class="sxs-lookup"><span data-stu-id="12b99-116">PARAMETERS</span></span>

### <span data-ttu-id="12b99-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="12b99-117">-Context</span></span>
<span data-ttu-id="12b99-118">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12b99-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="12b99-119">Você pode criá-lo usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="12b99-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="12b99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b99-120">-DefaultProfile</span></span>
<span data-ttu-id="12b99-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12b99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b99-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="12b99-122">-ExpiryTime</span></span>
<span data-ttu-id="12b99-123">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="12b99-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="12b99-124">Se o usuário definir a hora de início, mas não a hora de vencimento, o tempo de expiração será definido como a hora de início mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="12b99-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="12b99-125">Se nem a hora de início nem a hora de vencimento forem especificadas, o tempo de expiração será definido como a hora atual mais uma hora.</span><span class="sxs-lookup"><span data-stu-id="12b99-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="12b99-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="12b99-126">-FullUri</span></span>
<span data-ttu-id="12b99-127">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="12b99-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="12b99-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="12b99-128">-IPAddressOrRange</span></span>
<span data-ttu-id="12b99-129">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="12b99-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="12b99-130">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="12b99-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="12b99-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="12b99-131">-Name</span></span>
<span data-ttu-id="12b99-132">Especifica um nome de contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12b99-132">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="12b99-133">-Permissão</span><span class="sxs-lookup"><span data-stu-id="12b99-133">-Permission</span></span>
<span data-ttu-id="12b99-134">Especifica as permissões para um contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12b99-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="12b99-135">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="12b99-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="12b99-136">-Política</span><span class="sxs-lookup"><span data-stu-id="12b99-136">-Policy</span></span>
<span data-ttu-id="12b99-137">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="12b99-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="12b99-138">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="12b99-138">-Protocol</span></span>
<span data-ttu-id="12b99-139">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="12b99-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="12b99-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="12b99-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="12b99-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="12b99-141">HttpsOnly</span></span>
* <span data-ttu-id="12b99-142">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="12b99-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b99-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="12b99-143">-StartTime</span></span>
<span data-ttu-id="12b99-144">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="12b99-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="12b99-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b99-145">CommonParameters</span></span>
<span data-ttu-id="12b99-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b99-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b99-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b99-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b99-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12b99-148">INPUTS</span></span>

### <span data-ttu-id="12b99-149">System. String</span><span class="sxs-lookup"><span data-stu-id="12b99-149">System.String</span></span>

### <span data-ttu-id="12b99-150">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12b99-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12b99-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12b99-151">OUTPUTS</span></span>

### <span data-ttu-id="12b99-152">System. String</span><span class="sxs-lookup"><span data-stu-id="12b99-152">System.String</span></span>

## <span data-ttu-id="12b99-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12b99-153">NOTES</span></span>

## <span data-ttu-id="12b99-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12b99-154">RELATED LINKS</span></span>

[<span data-ttu-id="12b99-155">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="12b99-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
