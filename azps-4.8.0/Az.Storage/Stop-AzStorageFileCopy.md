---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: ac36914167bd5bda2e79576d9879d6f8c92ba7fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112048"
---
# <span data-ttu-id="90f6d-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="90f6d-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="90f6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="90f6d-103">Interrompe uma operação de cópia para o arquivo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="90f6d-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="90f6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90f6d-104">SYNTAX</span></span>

### <span data-ttu-id="90f6d-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="90f6d-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90f6d-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="90f6d-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f6d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90f6d-107">DESCRIPTION</span></span>
<span data-ttu-id="90f6d-108">O cmdlet **Stop-AzStorageFileCopy** interrompe a cópia de um arquivo para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="90f6d-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="90f6d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90f6d-109">EXAMPLES</span></span>

### <span data-ttu-id="90f6d-110">Exemplo 1: parar uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="90f6d-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="90f6d-111">Esse comando para de copiar um arquivo com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="90f6d-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="90f6d-112">OS</span><span class="sxs-lookup"><span data-stu-id="90f6d-112">PARAMETERS</span></span>

### <span data-ttu-id="90f6d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90f6d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="90f6d-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="90f6d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="90f6d-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="90f6d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="90f6d-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="90f6d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f6d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="90f6d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="90f6d-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="90f6d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="90f6d-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="90f6d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="90f6d-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="90f6d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="90f6d-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="90f6d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="90f6d-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="90f6d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="90f6d-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="90f6d-123">-Context</span></span>
<span data-ttu-id="90f6d-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="90f6d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90f6d-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="90f6d-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f6d-126">-Copyid</span><span class="sxs-lookup"><span data-stu-id="90f6d-126">-CopyId</span></span>
<span data-ttu-id="90f6d-127">Especifica a ID da operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="90f6d-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="90f6d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f6d-128">-DefaultProfile</span></span>
<span data-ttu-id="90f6d-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90f6d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90f6d-130">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="90f6d-130">-File</span></span>
<span data-ttu-id="90f6d-131">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="90f6d-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="90f6d-132">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="90f6d-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f6d-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="90f6d-133">-FilePath</span></span>
<span data-ttu-id="90f6d-134">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="90f6d-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f6d-135">-Force</span><span class="sxs-lookup"><span data-stu-id="90f6d-135">-Force</span></span>
<span data-ttu-id="90f6d-136">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="90f6d-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="90f6d-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90f6d-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="90f6d-138">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="90f6d-138">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f6d-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="90f6d-139">-ShareName</span></span>
<span data-ttu-id="90f6d-140">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="90f6d-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f6d-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90f6d-141">-Confirm</span></span>
<span data-ttu-id="90f6d-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f6d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f6d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f6d-143">-WhatIf</span></span>
<span data-ttu-id="90f6d-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90f6d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90f6d-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90f6d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f6d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f6d-146">CommonParameters</span></span>
<span data-ttu-id="90f6d-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f6d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f6d-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f6d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f6d-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90f6d-149">INPUTS</span></span>

### <span data-ttu-id="90f6d-150">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="90f6d-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="90f6d-151">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90f6d-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90f6d-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90f6d-152">OUTPUTS</span></span>

### <span data-ttu-id="90f6d-153">System. void</span><span class="sxs-lookup"><span data-stu-id="90f6d-153">System.Void</span></span>

## <span data-ttu-id="90f6d-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90f6d-154">NOTES</span></span>

## <span data-ttu-id="90f6d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90f6d-155">RELATED LINKS</span></span>

[<span data-ttu-id="90f6d-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="90f6d-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="90f6d-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="90f6d-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="90f6d-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="90f6d-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="90f6d-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="90f6d-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
