---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: b30a7736c1d3971bcdd4d7b3b776b0c439e9395b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887930"
---
# <span data-ttu-id="cc793-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="cc793-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="cc793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc793-102">SYNOPSIS</span></span>
<span data-ttu-id="cc793-103">Cria um objeto que representa um caminho de Armazenamento do Azure a ser montado em um Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="cc793-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="cc793-104">Ele deve ser usado como um parâmetro (-AzureStoragePath) para Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc793-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="cc793-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cc793-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc793-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cc793-106">DESCRIPTION</span></span>
<span data-ttu-id="cc793-107">Cria um objeto que representa um caminho de Armazenamento do Azure a ser montado dentro de um Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="cc793-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="cc793-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc793-108">EXAMPLES</span></span>

### <span data-ttu-id="cc793-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc793-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="cc793-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cc793-110">PARAMETERS</span></span>

### <span data-ttu-id="cc793-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="cc793-111">-AccessKey</span></span>
<span data-ttu-id="cc793-112">Chave de acesso à conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="cc793-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cc793-113">-AccountName</span></span>
<span data-ttu-id="cc793-114">Nome da conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc793-114">Azure Storage account name.</span></span>
<span data-ttu-id="cc793-115">Por exemplo: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="cc793-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc793-116">-DefaultProfile</span></span>
<span data-ttu-id="cc793-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc793-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="cc793-118">-MountPath</span></span>
<span data-ttu-id="cc793-119">Caminho no contêiner onde o compartilhamento especificado pelo ShareName será exposto</span><span class="sxs-lookup"><span data-stu-id="cc793-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cc793-120">-Name</span></span>
<span data-ttu-id="cc793-121">O identificador da propriedade Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc793-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="cc793-122">Deve ser exclusivo dentro do Aplicativo Web ou slot</span><span class="sxs-lookup"><span data-stu-id="cc793-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cc793-123">-ShareName</span></span>
<span data-ttu-id="cc793-124">Nome do compartilhamento a ser montado no contêiner</span><span class="sxs-lookup"><span data-stu-id="cc793-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-125">-Type</span><span class="sxs-lookup"><span data-stu-id="cc793-125">-Type</span></span>
<span data-ttu-id="cc793-126">Tipo de conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc793-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="cc793-127">Contêineres do Windows só suportam arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="cc793-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc793-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc793-128">-Confirm</span></span>
<span data-ttu-id="cc793-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc793-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc793-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc793-130">-WhatIf</span></span>
<span data-ttu-id="cc793-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc793-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc793-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc793-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc793-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc793-133">CommonParameters</span></span>
<span data-ttu-id="cc793-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc793-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc793-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc793-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc793-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc793-136">INPUTS</span></span>

### <span data-ttu-id="cc793-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cc793-137">None</span></span>

## <span data-ttu-id="cc793-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cc793-138">OUTPUTS</span></span>

### <span data-ttu-id="cc793-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="cc793-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="cc793-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="cc793-140">NOTES</span></span>

## <span data-ttu-id="cc793-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc793-141">RELATED LINKS</span></span>
