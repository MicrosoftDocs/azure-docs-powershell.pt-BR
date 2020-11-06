---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 0ddfbd8aceeb26a4f40fcf104919fa9b67b39aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426452"
---
# <span data-ttu-id="23968-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="23968-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="23968-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23968-102">SYNOPSIS</span></span>
<span data-ttu-id="23968-103">Importa um módulo para a automação.</span><span class="sxs-lookup"><span data-stu-id="23968-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23968-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23968-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23968-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23968-105">DESCRIPTION</span></span>
<span data-ttu-id="23968-106">O cmdlet **New-AzureRmAutomationModule** importa um módulo para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="23968-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="23968-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="23968-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="23968-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="23968-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="23968-109">wps_2 módulo, que tem a extensão de nome de arquivo. psm1 ou. dll</span><span class="sxs-lookup"><span data-stu-id="23968-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="23968-110">wps_2 manifesto do módulo, que tem a extensão de nome de arquivo. psd1, o nome do arquivo. zip, o nome da pasta e o nome do arquivo na pasta devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="23968-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="23968-111">Especifique o arquivo. zip como uma URL que o serviço de automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="23968-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="23968-112">Se você importar um módulo wps_2 para a automação usando este cmdlet ou o cmdlet Set-AzureRmAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="23968-112">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="23968-113">O comando termina se a importação tiver êxito ou falhará.</span><span class="sxs-lookup"><span data-stu-id="23968-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="23968-114">Para verificar se foi bem-sucedida, execute o seguinte comando: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name ` ModuleName Verifique a propriedade **ProvisioningState** para obter um valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="23968-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="23968-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23968-115">EXAMPLES</span></span>

### <span data-ttu-id="23968-116">Exemplo 1: importar um módulo</span><span class="sxs-lookup"><span data-stu-id="23968-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="23968-117">Esse comando importa um módulo chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="23968-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="23968-118">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.</span><span class="sxs-lookup"><span data-stu-id="23968-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="23968-119">OS</span><span class="sxs-lookup"><span data-stu-id="23968-119">PARAMETERS</span></span>

### <span data-ttu-id="23968-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23968-120">-AutomationAccountName</span></span>
<span data-ttu-id="23968-121">Especifica o nome da conta de automação para a qual esse cmdlet importa um módulo.</span><span class="sxs-lookup"><span data-stu-id="23968-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="23968-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="23968-122">-ContentLinkUri</span></span>
<span data-ttu-id="23968-123">A URL para um pacote zip de módulo</span><span class="sxs-lookup"><span data-stu-id="23968-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23968-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23968-124">-DefaultProfile</span></span>
<span data-ttu-id="23968-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="23968-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23968-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="23968-126">-Name</span></span>
<span data-ttu-id="23968-127">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="23968-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="23968-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23968-128">-ResourceGroupName</span></span>
<span data-ttu-id="23968-129">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa um módulo.</span><span class="sxs-lookup"><span data-stu-id="23968-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="23968-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23968-130">CommonParameters</span></span>
<span data-ttu-id="23968-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23968-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23968-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23968-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23968-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23968-133">INPUTS</span></span>

### <span data-ttu-id="23968-134">System. String</span><span class="sxs-lookup"><span data-stu-id="23968-134">System.String</span></span>

### <span data-ttu-id="23968-135">System. URI</span><span class="sxs-lookup"><span data-stu-id="23968-135">System.Uri</span></span>

## <span data-ttu-id="23968-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23968-136">OUTPUTS</span></span>

### <span data-ttu-id="23968-137">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="23968-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="23968-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23968-138">NOTES</span></span>

## <span data-ttu-id="23968-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23968-139">RELATED LINKS</span></span>

[<span data-ttu-id="23968-140">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="23968-140">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="23968-141">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="23968-141">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="23968-142">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="23968-142">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


