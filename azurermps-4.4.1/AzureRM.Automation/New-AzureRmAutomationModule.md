---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441418"
---
# <span data-ttu-id="e3890-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e3890-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="e3890-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3890-102">SYNOPSIS</span></span>
<span data-ttu-id="e3890-103">Importa um módulo para a automação.</span><span class="sxs-lookup"><span data-stu-id="e3890-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3890-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3890-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3890-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3890-105">DESCRIPTION</span></span>
<span data-ttu-id="e3890-106">O cmdlet **New-AzureRmAutomationModule** importa um módulo para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3890-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="e3890-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="e3890-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="e3890-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="e3890-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="e3890-109">wps_2 módulo, que tem a extensão de nome de arquivo. psm1 ou. dll</span><span class="sxs-lookup"><span data-stu-id="e3890-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="e3890-110">manifesto do módulo wps_2, que tem uma extensão de nome de arquivo. psd1</span><span class="sxs-lookup"><span data-stu-id="e3890-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="e3890-111">O nome do arquivo. zip, o nome da pasta e o nome do arquivo na pasta devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="e3890-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="e3890-112">Especifique o arquivo. zip como uma URL que o serviço de automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="e3890-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="e3890-113">Se você importar um módulo wps_2 para a automação usando este cmdlet ou o cmdlet Set-AzureRmAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e3890-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="e3890-114">O comando termina se a importação tiver êxito ou falhará.</span><span class="sxs-lookup"><span data-stu-id="e3890-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="e3890-115">Para verificar se foi bem-sucedida, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="e3890-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="e3890-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="e3890-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="e3890-117">Verifique se a propriedade **ProvisioningState** tem um valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="e3890-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="e3890-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3890-118">EXAMPLES</span></span>

### <span data-ttu-id="e3890-119">Exemplo 1: importar um módulo</span><span class="sxs-lookup"><span data-stu-id="e3890-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e3890-120">Esse comando importa um módulo chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e3890-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="e3890-121">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.</span><span class="sxs-lookup"><span data-stu-id="e3890-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="e3890-122">OS</span><span class="sxs-lookup"><span data-stu-id="e3890-122">PARAMETERS</span></span>

### <span data-ttu-id="e3890-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3890-123">-AutomationAccountName</span></span>
<span data-ttu-id="e3890-124">Especifica o nome da conta de automação para a qual esse cmdlet importa um módulo.</span><span class="sxs-lookup"><span data-stu-id="e3890-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="e3890-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="e3890-125">-ContentLinkUri</span></span>
<span data-ttu-id="e3890-126">A URL para um pacote zip de módulo.</span><span class="sxs-lookup"><span data-stu-id="e3890-126">The url to a module zip package.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3890-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3890-127">-Name</span></span>
<span data-ttu-id="e3890-128">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="e3890-128">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3890-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3890-129">-ResourceGroupName</span></span>
<span data-ttu-id="e3890-130">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa um módulo.</span><span class="sxs-lookup"><span data-stu-id="e3890-130">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3890-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3890-131">-DefaultProfile</span></span>
<span data-ttu-id="e3890-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3890-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3890-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3890-133">CommonParameters</span></span>
<span data-ttu-id="e3890-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3890-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3890-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3890-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3890-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3890-136">INPUTS</span></span>

## <span data-ttu-id="e3890-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3890-137">OUTPUTS</span></span>

### <span data-ttu-id="e3890-138">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="e3890-138">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="e3890-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3890-139">NOTES</span></span>

## <span data-ttu-id="e3890-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3890-140">RELATED LINKS</span></span>

[<span data-ttu-id="e3890-141">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e3890-141">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="e3890-142">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e3890-142">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="e3890-143">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e3890-143">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


