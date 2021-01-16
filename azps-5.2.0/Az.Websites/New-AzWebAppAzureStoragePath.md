---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258040"
---
# <span data-ttu-id="1798f-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="1798f-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="1798f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1798f-102">SYNOPSIS</span></span>
<span data-ttu-id="1798f-103">Cria um objeto que representa um caminho de armazenamento do Azure a ser montado em um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1798f-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="1798f-104">Ele deve ser usado como um parâmetro (-AzureStoragePath) para Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1798f-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="1798f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1798f-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1798f-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1798f-106">DESCRIPTION</span></span>
<span data-ttu-id="1798f-107">Cria um objeto que representa um caminho de armazenamento do Azure a ser montado dentro de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1798f-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="1798f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1798f-108">EXAMPLES</span></span>

### <span data-ttu-id="1798f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1798f-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="1798f-110">OS</span><span class="sxs-lookup"><span data-stu-id="1798f-110">PARAMETERS</span></span>

### <span data-ttu-id="1798f-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="1798f-111">-AccessKey</span></span>
<span data-ttu-id="1798f-112">Tecla de acesso para a conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="1798f-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="1798f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1798f-113">-AccountName</span></span>
<span data-ttu-id="1798f-114">Nome da conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1798f-114">Azure Storage account name.</span></span>
<span data-ttu-id="1798f-115">Por exemplo: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="1798f-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="1798f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1798f-116">-DefaultProfile</span></span>
<span data-ttu-id="1798f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1798f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1798f-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="1798f-118">-MountPath</span></span>
<span data-ttu-id="1798f-119">Caminho no contêiner em que o compartilhamento especificado por ShareName será exposto</span><span class="sxs-lookup"><span data-stu-id="1798f-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="1798f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1798f-120">-Name</span></span>
<span data-ttu-id="1798f-121">O identificador da propriedade de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1798f-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="1798f-122">Deve ser exclusivo no aplicativo Web ou no slot</span><span class="sxs-lookup"><span data-stu-id="1798f-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="1798f-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1798f-123">-ShareName</span></span>
<span data-ttu-id="1798f-124">Nome do compartilhamento para montar no contêiner</span><span class="sxs-lookup"><span data-stu-id="1798f-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="1798f-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="1798f-125">-Type</span></span>
<span data-ttu-id="1798f-126">Tipo de conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1798f-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="1798f-127">Os contêineres do Windows só dão suporte a arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="1798f-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="1798f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1798f-128">-Confirm</span></span>
<span data-ttu-id="1798f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1798f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1798f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1798f-130">-WhatIf</span></span>
<span data-ttu-id="1798f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1798f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1798f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1798f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1798f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1798f-133">CommonParameters</span></span>
<span data-ttu-id="1798f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1798f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1798f-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1798f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1798f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1798f-136">INPUTS</span></span>

### <span data-ttu-id="1798f-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1798f-137">None</span></span>

## <span data-ttu-id="1798f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1798f-138">OUTPUTS</span></span>

### <span data-ttu-id="1798f-139">Microsoft. Azure. Commands. webapps. Models. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="1798f-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="1798f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1798f-140">NOTES</span></span>

## <span data-ttu-id="1798f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1798f-141">RELATED LINKS</span></span>
