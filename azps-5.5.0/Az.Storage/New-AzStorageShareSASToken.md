---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118578"
---
# <span data-ttu-id="9f38a-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="9f38a-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="9f38a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f38a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f38a-103">Gere um token de Assinatura de Acesso Compartilhado para o compartilhamento de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f38a-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="9f38a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f38a-104">SYNTAX</span></span>

### <span data-ttu-id="9f38a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="9f38a-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f38a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="9f38a-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f38a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f38a-107">DESCRIPTION</span></span>
<span data-ttu-id="9f38a-108">O cmdlet **New-AzStorageShareSASToken** gera um token de assinatura de acesso compartilhado para um compartilhamento de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f38a-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="9f38a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f38a-109">EXAMPLES</span></span>

### <span data-ttu-id="9f38a-110">Exemplo 1: Gerar um token de assinatura de acesso compartilhado para um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="9f38a-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="9f38a-111">Esse comando cria um token de assinatura de acesso compartilhado para o compartilhamento chamado ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="9f38a-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="9f38a-112">Exemplo 2: Gerar vários tokens de assinatura de acesso compartilhado usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="9f38a-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="9f38a-113">Esse comando obtém todos os compartilhamentos de Armazenamento que corresponderem ao teste de prefixo.</span><span class="sxs-lookup"><span data-stu-id="9f38a-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="9f38a-114">O comando passa-os para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f38a-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f38a-115">O cmdlet atual cria um token de acesso compartilhado para cada compartilhamento de Armazenamento que tenha as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="9f38a-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="9f38a-116">Exemplo 3: Gerar um token de assinatura de acesso compartilhado que usa uma política de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="9f38a-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="9f38a-117">Esse comando cria um token de assinatura de acesso compartilhado para o compartilhamento de armazenamento chamado ContosoShare que tem a política chamada ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="9f38a-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="9f38a-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f38a-118">PARAMETERS</span></span>

### <span data-ttu-id="9f38a-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9f38a-119">-Context</span></span>
<span data-ttu-id="9f38a-120">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f38a-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9f38a-121">Para obter um contexto, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f38a-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9f38a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f38a-122">-DefaultProfile</span></span>
<span data-ttu-id="9f38a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f38a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f38a-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9f38a-124">-ExpiryTime</span></span>
<span data-ttu-id="9f38a-125">Especifica o momento em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="9f38a-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="9f38a-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="9f38a-126">-FullUri</span></span>
<span data-ttu-id="9f38a-127">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="9f38a-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="9f38a-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9f38a-128">-IPAddressOrRange</span></span>
<span data-ttu-id="9f38a-129">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="9f38a-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9f38a-130">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="9f38a-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="9f38a-131">-Permissão</span><span class="sxs-lookup"><span data-stu-id="9f38a-131">-Permission</span></span>
<span data-ttu-id="9f38a-132">Especifica as permissões no token para acessar o compartilhamento e os arquivos sob o compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="9f38a-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="9f38a-133">É importante observar que esta é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="9f38a-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="9f38a-134">-Política</span><span class="sxs-lookup"><span data-stu-id="9f38a-134">-Policy</span></span>
<span data-ttu-id="9f38a-135">Especifica a política de acesso armazenada para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="9f38a-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="9f38a-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="9f38a-136">-Protocol</span></span>
<span data-ttu-id="9f38a-137">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9f38a-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="9f38a-138">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9f38a-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="9f38a-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9f38a-139">HttpsOnly</span></span>
* <span data-ttu-id="9f38a-140">HttpsOrHttp O valor padrão é httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9f38a-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="9f38a-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9f38a-141">-ShareName</span></span>
<span data-ttu-id="9f38a-142">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9f38a-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f38a-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9f38a-143">-StartTime</span></span>
<span data-ttu-id="9f38a-144">Especifica o momento em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="9f38a-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="9f38a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f38a-145">CommonParameters</span></span>
<span data-ttu-id="9f38a-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f38a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f38a-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f38a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f38a-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f38a-148">INPUTS</span></span>

### <span data-ttu-id="9f38a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9f38a-149">System.String</span></span>

### <span data-ttu-id="9f38a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9f38a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9f38a-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f38a-151">OUTPUTS</span></span>

### <span data-ttu-id="9f38a-152">System.String</span><span class="sxs-lookup"><span data-stu-id="9f38a-152">System.String</span></span>

## <span data-ttu-id="9f38a-153">Notas</span><span class="sxs-lookup"><span data-stu-id="9f38a-153">NOTES</span></span>
* <span data-ttu-id="9f38a-154">Palavras-chave: comum, azure, serviços, dados, armazenamento, blob, fila, tabela</span><span class="sxs-lookup"><span data-stu-id="9f38a-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="9f38a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f38a-155">RELATED LINKS</span></span>

[<span data-ttu-id="9f38a-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="9f38a-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="9f38a-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="9f38a-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
