---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: e58b9d98a2e185b39c64e999f95e45c610da0f3d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776176"
---
# <span data-ttu-id="1eff5-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1eff5-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="1eff5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eff5-102">SYNOPSIS</span></span>
<span data-ttu-id="1eff5-103">Remove uma política de acesso armazenado de um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1eff5-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="1eff5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eff5-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1eff5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eff5-105">DESCRIPTION</span></span>
<span data-ttu-id="1eff5-106">O cmdlet **Remove-AzStorageShareStoredAccessPolicy** remove uma política de acesso armazenado de um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eff5-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="1eff5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eff5-107">EXAMPLES</span></span>

### <span data-ttu-id="1eff5-108">Exemplo 1: remover uma política de acesso armazenado de um compartilhamento de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="1eff5-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="1eff5-109">Esse comando Remove uma política de acesso armazenado chamada GeneralPolicy do ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="1eff5-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="1eff5-110">OS</span><span class="sxs-lookup"><span data-stu-id="1eff5-110">PARAMETERS</span></span>

### <span data-ttu-id="1eff5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1eff5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1eff5-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1eff5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1eff5-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1eff5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1eff5-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1eff5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1eff5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1eff5-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1eff5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1eff5-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1eff5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1eff5-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1eff5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1eff5-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1eff5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1eff5-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1eff5-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1eff5-121">-Context</span></span>
<span data-ttu-id="1eff5-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eff5-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1eff5-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="1eff5-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1eff5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eff5-124">-DefaultProfile</span></span>
<span data-ttu-id="1eff5-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eff5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eff5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1eff5-126">-PassThru</span></span>
<span data-ttu-id="1eff5-127">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="1eff5-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1eff5-128">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1eff5-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1eff5-129">-Política</span><span class="sxs-lookup"><span data-stu-id="1eff5-129">-Policy</span></span>
<span data-ttu-id="1eff5-130">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1eff5-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1eff5-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1eff5-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="1eff5-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1eff5-133">-ShareName</span></span>
<span data-ttu-id="1eff5-134">Especifica o nome do compartilhamento de armazenamento para o qual esse cmdlet Remove uma política.</span><span class="sxs-lookup"><span data-stu-id="1eff5-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1eff5-135">-Confirm</span></span>
<span data-ttu-id="1eff5-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eff5-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eff5-137">-WhatIf</span></span>
<span data-ttu-id="1eff5-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1eff5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eff5-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1eff5-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eff5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eff5-140">CommonParameters</span></span>
<span data-ttu-id="1eff5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eff5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eff5-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eff5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eff5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eff5-143">INPUTS</span></span>

### <span data-ttu-id="1eff5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1eff5-144">System.String</span></span>

### <span data-ttu-id="1eff5-145">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1eff5-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1eff5-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eff5-146">OUTPUTS</span></span>

### <span data-ttu-id="1eff5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1eff5-147">System.Boolean</span></span>

## <span data-ttu-id="1eff5-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eff5-148">NOTES</span></span>

## <span data-ttu-id="1eff5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eff5-149">RELATED LINKS</span></span>

[<span data-ttu-id="1eff5-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1eff5-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1eff5-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1eff5-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="1eff5-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1eff5-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1eff5-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1eff5-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)