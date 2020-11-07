---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 2ae003eaa20ddcc42fa31ab14c64f78255140c29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772786"
---
# <span data-ttu-id="08889-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="08889-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="08889-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08889-102">SYNOPSIS</span></span>
<span data-ttu-id="08889-103">Gera um token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="08889-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="08889-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08889-104">SYNTAX</span></span>

### <span data-ttu-id="08889-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="08889-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08889-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="08889-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08889-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08889-107">DESCRIPTION</span></span>
<span data-ttu-id="08889-108">O cmdlet **New-AzStorageQueueSASToken** gera token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="08889-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="08889-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08889-109">EXAMPLES</span></span>

### <span data-ttu-id="08889-110">Exemplo 1: gerar um token SAS de fila com permissão completa</span><span class="sxs-lookup"><span data-stu-id="08889-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="08889-111">Este exemplo gera um token SAS de fila com permissão completa.</span><span class="sxs-lookup"><span data-stu-id="08889-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="08889-112">OS</span><span class="sxs-lookup"><span data-stu-id="08889-112">PARAMETERS</span></span>

### <span data-ttu-id="08889-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="08889-113">-Context</span></span>
<span data-ttu-id="08889-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="08889-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="08889-115">Você pode criá-lo por New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08889-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="08889-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08889-116">-DefaultProfile</span></span>
<span data-ttu-id="08889-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08889-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08889-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="08889-118">-ExpiryTime</span></span>
<span data-ttu-id="08889-119">Especifica quando a assinatura de acesso compartilhado não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="08889-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="08889-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="08889-120">-FullUri</span></span>
<span data-ttu-id="08889-121">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="08889-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="08889-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="08889-122">-IPAddressOrRange</span></span>
<span data-ttu-id="08889-123">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="08889-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="08889-124">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="08889-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="08889-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="08889-125">-Name</span></span>
<span data-ttu-id="08889-126">Especifica um nome de fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="08889-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="08889-127">-Permissão</span><span class="sxs-lookup"><span data-stu-id="08889-127">-Permission</span></span>
<span data-ttu-id="08889-128">Especifica as permissões para uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="08889-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="08889-129">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="08889-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="08889-130">-Política</span><span class="sxs-lookup"><span data-stu-id="08889-130">-Policy</span></span>
<span data-ttu-id="08889-131">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="08889-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="08889-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="08889-132">-Protocol</span></span>
<span data-ttu-id="08889-133">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="08889-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="08889-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08889-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="08889-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="08889-135">HttpsOnly</span></span>
* <span data-ttu-id="08889-136">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="08889-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="08889-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="08889-137">-StartTime</span></span>
<span data-ttu-id="08889-138">Especifica quando a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="08889-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="08889-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08889-139">CommonParameters</span></span>
<span data-ttu-id="08889-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08889-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08889-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08889-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08889-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08889-142">INPUTS</span></span>

### <span data-ttu-id="08889-143">System. String</span><span class="sxs-lookup"><span data-stu-id="08889-143">System.String</span></span>

### <span data-ttu-id="08889-144">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="08889-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="08889-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08889-145">OUTPUTS</span></span>

### <span data-ttu-id="08889-146">System. String</span><span class="sxs-lookup"><span data-stu-id="08889-146">System.String</span></span>

## <span data-ttu-id="08889-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08889-147">NOTES</span></span>

## <span data-ttu-id="08889-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08889-148">RELATED LINKS</span></span>