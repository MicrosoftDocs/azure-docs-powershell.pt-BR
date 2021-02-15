---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112330"
---
# <span data-ttu-id="ca739-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ca739-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="ca739-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca739-102">SYNOPSIS</span></span>
<span data-ttu-id="ca739-103">Cria um objeto que representa um caminho de Armazenamento do Azure a ser montado em um Web App.</span><span class="sxs-lookup"><span data-stu-id="ca739-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="ca739-104">Ele deve ser usado como um parâmetro (-AzureStoragePath) para Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ca739-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="ca739-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca739-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca739-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca739-106">DESCRIPTION</span></span>
<span data-ttu-id="ca739-107">Cria um objeto que representa um caminho de Armazenamento do Azure a ser montado dentro de um Web App.</span><span class="sxs-lookup"><span data-stu-id="ca739-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="ca739-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca739-108">EXAMPLES</span></span>

### <span data-ttu-id="ca739-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca739-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="ca739-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca739-110">PARAMETERS</span></span>

### <span data-ttu-id="ca739-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="ca739-111">-AccessKey</span></span>
<span data-ttu-id="ca739-112">Tecla de acesso à conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="ca739-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="ca739-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="ca739-113">-AccountName</span></span>
<span data-ttu-id="ca739-114">Nome da conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca739-114">Azure Storage account name.</span></span>
<span data-ttu-id="ca739-115">Por exemplo: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ca739-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="ca739-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca739-116">-DefaultProfile</span></span>
<span data-ttu-id="ca739-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca739-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca739-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="ca739-118">-MountPath</span></span>
<span data-ttu-id="ca739-119">Caminho no contêiner onde o compartilhamento especificado pelo ShareName será exposto</span><span class="sxs-lookup"><span data-stu-id="ca739-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="ca739-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca739-120">-Name</span></span>
<span data-ttu-id="ca739-121">O identificador da propriedade Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca739-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="ca739-122">Deve ser exclusivo no Aplicativo Web ou no Slot</span><span class="sxs-lookup"><span data-stu-id="ca739-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="ca739-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ca739-123">-ShareName</span></span>
<span data-ttu-id="ca739-124">Nome do compartilhamento a ser montado no contêiner</span><span class="sxs-lookup"><span data-stu-id="ca739-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="ca739-125">-Tipo</span><span class="sxs-lookup"><span data-stu-id="ca739-125">-Type</span></span>
<span data-ttu-id="ca739-126">Tipo de conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca739-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="ca739-127">Os Contêineres do Windows só são compatíveis com Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="ca739-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="ca739-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ca739-128">-Confirm</span></span>
<span data-ttu-id="ca739-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca739-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca739-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca739-130">-WhatIf</span></span>
<span data-ttu-id="ca739-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ca739-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca739-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca739-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca739-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca739-133">CommonParameters</span></span>
<span data-ttu-id="ca739-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca739-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca739-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca739-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca739-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca739-136">INPUTS</span></span>

### <span data-ttu-id="ca739-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ca739-137">None</span></span>

## <span data-ttu-id="ca739-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca739-138">OUTPUTS</span></span>

### <span data-ttu-id="ca739-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="ca739-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="ca739-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ca739-140">NOTES</span></span>

## <span data-ttu-id="ca739-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca739-141">RELATED LINKS</span></span>
