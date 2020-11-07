---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 4c3715a3c6228e45bfa52fd9a222be2cae84ef01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776217"
---
# <span data-ttu-id="206b9-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="206b9-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="206b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="206b9-102">SYNOPSIS</span></span>
<span data-ttu-id="206b9-103">Gera um token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="206b9-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="206b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="206b9-104">SYNTAX</span></span>

### <span data-ttu-id="206b9-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="206b9-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="206b9-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="206b9-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="206b9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="206b9-107">DESCRIPTION</span></span>
<span data-ttu-id="206b9-108">O cmdlet **New-AzStorageQueueSASToken** gera token de assinatura de acesso compartilhado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="206b9-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="206b9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="206b9-109">EXAMPLES</span></span>

### <span data-ttu-id="206b9-110">Exemplo 1: gerar um token SAS de fila com permissão completa</span><span class="sxs-lookup"><span data-stu-id="206b9-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="206b9-111">Este exemplo gera um token SAS de fila com permissão completa.</span><span class="sxs-lookup"><span data-stu-id="206b9-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="206b9-112">OS</span><span class="sxs-lookup"><span data-stu-id="206b9-112">PARAMETERS</span></span>

### <span data-ttu-id="206b9-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="206b9-113">-Context</span></span>
<span data-ttu-id="206b9-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="206b9-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="206b9-115">Você pode criá-lo por New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="206b9-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="206b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206b9-116">-DefaultProfile</span></span>
<span data-ttu-id="206b9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="206b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206b9-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="206b9-118">-ExpiryTime</span></span>
<span data-ttu-id="206b9-119">Especifica quando a assinatura de acesso compartilhado não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="206b9-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="206b9-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="206b9-120">-FullUri</span></span>
<span data-ttu-id="206b9-121">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="206b9-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="206b9-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="206b9-122">-IPAddressOrRange</span></span>
<span data-ttu-id="206b9-123">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="206b9-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="206b9-124">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="206b9-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="206b9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="206b9-125">-Name</span></span>
<span data-ttu-id="206b9-126">Especifica um nome de fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="206b9-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="206b9-127">-Permissão</span><span class="sxs-lookup"><span data-stu-id="206b9-127">-Permission</span></span>
<span data-ttu-id="206b9-128">Especifica as permissões para uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="206b9-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="206b9-129">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="206b9-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="206b9-130">-Política</span><span class="sxs-lookup"><span data-stu-id="206b9-130">-Policy</span></span>
<span data-ttu-id="206b9-131">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="206b9-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="206b9-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="206b9-132">-Protocol</span></span>
<span data-ttu-id="206b9-133">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="206b9-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="206b9-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="206b9-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="206b9-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="206b9-135">HttpsOnly</span></span>
* <span data-ttu-id="206b9-136">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="206b9-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206b9-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="206b9-137">-StartTime</span></span>
<span data-ttu-id="206b9-138">Especifica quando a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="206b9-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="206b9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206b9-139">CommonParameters</span></span>
<span data-ttu-id="206b9-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206b9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206b9-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206b9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206b9-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="206b9-142">INPUTS</span></span>

### <span data-ttu-id="206b9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="206b9-143">System.String</span></span>

### <span data-ttu-id="206b9-144">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="206b9-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="206b9-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="206b9-145">OUTPUTS</span></span>

### <span data-ttu-id="206b9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="206b9-146">System.String</span></span>

## <span data-ttu-id="206b9-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="206b9-147">NOTES</span></span>

## <span data-ttu-id="206b9-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="206b9-148">RELATED LINKS</span></span>
