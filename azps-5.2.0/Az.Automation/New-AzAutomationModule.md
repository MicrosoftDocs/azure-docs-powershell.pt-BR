---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264560"
---
# <span data-ttu-id="9636b-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9636b-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="9636b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9636b-102">SYNOPSIS</span></span>
<span data-ttu-id="9636b-103">Importa um módulo para a automação.</span><span class="sxs-lookup"><span data-stu-id="9636b-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="9636b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9636b-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9636b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9636b-105">DESCRIPTION</span></span>
<span data-ttu-id="9636b-106">O cmdlet **New-AzAutomationModule** importa um módulo para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9636b-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="9636b-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="9636b-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="9636b-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="9636b-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="9636b-109">Módulo do Windows PowerShell, que tem a extensão de nome de arquivo. psm1 ou. dll</span><span class="sxs-lookup"><span data-stu-id="9636b-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="9636b-110">Manifesto do módulo do Windows PowerShell, que tem a extensão de nome de arquivo. psd1, o nome do arquivo. zip, o nome da pasta e o nome do arquivo na pasta devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="9636b-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="9636b-111">Especifique o arquivo. zip como uma URL que o serviço de automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="9636b-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="9636b-112">Se você importar um módulo do Windows PowerShell para automação usando este cmdlet ou o cmdlet Set-AzAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9636b-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="9636b-113">O comando termina se a importação tiver êxito ou falhará.</span><span class="sxs-lookup"><span data-stu-id="9636b-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="9636b-114">Para verificar se foi bem-sucedida, execute o seguinte comando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Verifique a propriedade **ProvisioningState** para obter um valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="9636b-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="9636b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9636b-115">EXAMPLES</span></span>

### <span data-ttu-id="9636b-116">Exemplo 1: importar um módulo</span><span class="sxs-lookup"><span data-stu-id="9636b-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9636b-117">Esse comando importa um módulo chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9636b-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="9636b-118">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.</span><span class="sxs-lookup"><span data-stu-id="9636b-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="9636b-119">OS</span><span class="sxs-lookup"><span data-stu-id="9636b-119">PARAMETERS</span></span>

### <span data-ttu-id="9636b-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9636b-120">-AutomationAccountName</span></span>
<span data-ttu-id="9636b-121">Especifica o nome da conta de automação para a qual esse cmdlet importa um módulo.</span><span class="sxs-lookup"><span data-stu-id="9636b-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="9636b-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="9636b-122">-ContentLinkUri</span></span>
<span data-ttu-id="9636b-123">A URL para um pacote zip de módulo</span><span class="sxs-lookup"><span data-stu-id="9636b-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="9636b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9636b-124">-DefaultProfile</span></span>
<span data-ttu-id="9636b-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9636b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9636b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9636b-126">-Name</span></span>
<span data-ttu-id="9636b-127">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="9636b-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9636b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9636b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9636b-129">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa um módulo.</span><span class="sxs-lookup"><span data-stu-id="9636b-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="9636b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9636b-130">CommonParameters</span></span>
<span data-ttu-id="9636b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9636b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9636b-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9636b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9636b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9636b-133">INPUTS</span></span>

### <span data-ttu-id="9636b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9636b-134">System.String</span></span>

### <span data-ttu-id="9636b-135">System. URI</span><span class="sxs-lookup"><span data-stu-id="9636b-135">System.Uri</span></span>

## <span data-ttu-id="9636b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9636b-136">OUTPUTS</span></span>

### <span data-ttu-id="9636b-137">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="9636b-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9636b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9636b-138">NOTES</span></span>

## <span data-ttu-id="9636b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9636b-139">RELATED LINKS</span></span>

[<span data-ttu-id="9636b-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9636b-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="9636b-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9636b-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="9636b-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9636b-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


