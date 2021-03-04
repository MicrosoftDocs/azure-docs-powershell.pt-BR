---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 3ecea2e4eece9b4e0161a90cc597218d04a29bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891952"
---
# <span data-ttu-id="17f8f-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="17f8f-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="17f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="17f8f-103">Gera um token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8f-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="17f8f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17f8f-104">SYNTAX</span></span>

### <span data-ttu-id="17f8f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="17f8f-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f8f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="17f8f-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f8f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17f8f-107">DESCRIPTION</span></span>
<span data-ttu-id="17f8f-108">O cmdlet **New-AzStorageQueueSASToken** gera um token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8f-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="17f8f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17f8f-109">EXAMPLES</span></span>

### <span data-ttu-id="17f8f-110">Exemplo 1: Gerar um token SAS de fila com permissão total</span><span class="sxs-lookup"><span data-stu-id="17f8f-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="17f8f-111">Este exemplo gera um token SAS de fila com permissão total.</span><span class="sxs-lookup"><span data-stu-id="17f8f-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="17f8f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17f8f-112">PARAMETERS</span></span>

### <span data-ttu-id="17f8f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="17f8f-113">-Context</span></span>
<span data-ttu-id="17f8f-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8f-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="17f8f-115">Você pode criar por meio New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17f8f-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="17f8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f8f-116">-DefaultProfile</span></span>
<span data-ttu-id="17f8f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17f8f-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="17f8f-118">-ExpiryTime</span></span>
<span data-ttu-id="17f8f-119">Especifica quando a assinatura de acesso compartilhado não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="17f8f-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="17f8f-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="17f8f-120">-FullUri</span></span>
<span data-ttu-id="17f8f-121">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="17f8f-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="17f8f-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="17f8f-122">-IPAddressOrRange</span></span>
<span data-ttu-id="17f8f-123">Especifica o endereço IP ou intervalo de endereços IP dos quais aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="17f8f-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="17f8f-124">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="17f8f-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="17f8f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="17f8f-125">-Name</span></span>
<span data-ttu-id="17f8f-126">Especifica um nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8f-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17f8f-127">-Permission</span><span class="sxs-lookup"><span data-stu-id="17f8f-127">-Permission</span></span>
<span data-ttu-id="17f8f-128">Especifica permissões para uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="17f8f-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="17f8f-129">É importante observar que esta é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="17f8f-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="17f8f-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="17f8f-130">-Policy</span></span>
<span data-ttu-id="17f8f-131">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8f-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="17f8f-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="17f8f-132">-Protocol</span></span>
<span data-ttu-id="17f8f-133">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="17f8f-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="17f8f-134">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="17f8f-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="17f8f-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="17f8f-135">HttpsOnly</span></span>
* <span data-ttu-id="17f8f-136">HttpsOrHttp O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="17f8f-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="17f8f-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="17f8f-137">-StartTime</span></span>
<span data-ttu-id="17f8f-138">Especifica quando a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="17f8f-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="17f8f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f8f-139">CommonParameters</span></span>
<span data-ttu-id="17f8f-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f8f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f8f-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f8f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f8f-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17f8f-142">INPUTS</span></span>

### <span data-ttu-id="17f8f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="17f8f-143">System.String</span></span>

### <span data-ttu-id="17f8f-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="17f8f-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="17f8f-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17f8f-145">OUTPUTS</span></span>

### <span data-ttu-id="17f8f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="17f8f-146">System.String</span></span>

## <span data-ttu-id="17f8f-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="17f8f-147">NOTES</span></span>

## <span data-ttu-id="17f8f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17f8f-148">RELATED LINKS</span></span>
