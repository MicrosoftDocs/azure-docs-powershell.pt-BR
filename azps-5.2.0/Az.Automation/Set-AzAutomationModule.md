---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264490"
---
# <span data-ttu-id="a03bc-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a03bc-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="a03bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a03bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a03bc-103">Atualiza um módulo na automação.</span><span class="sxs-lookup"><span data-stu-id="a03bc-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="a03bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a03bc-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a03bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a03bc-105">DESCRIPTION</span></span>
<span data-ttu-id="a03bc-106">O cmdlet **set-AzAutomationModule** atualiza um módulo na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a03bc-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="a03bc-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="a03bc-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="a03bc-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="a03bc-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="a03bc-109">wps_2 módulo, que tem a extensão de nome de arquivo. psm1 ou. dll</span><span class="sxs-lookup"><span data-stu-id="a03bc-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="a03bc-110">wps_2 manifesto do módulo, que tem a extensão de nome de arquivo. psd1, o nome do arquivo. zip, o nome da pasta e o nome do arquivo na pasta devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="a03bc-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="a03bc-111">Especifique o arquivo. zip como uma URL que o serviço de automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="a03bc-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="a03bc-112">Se você importar um módulo wps_2 para a automação usando este cmdlet ou o cmdlet New-AzAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a03bc-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="a03bc-113">O comando termina se a importação tiver êxito ou falhará.</span><span class="sxs-lookup"><span data-stu-id="a03bc-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="a03bc-114">Para verificar se foi bem-sucedida, execute o seguinte comando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Verifique a propriedade **ProvisioningState** para obter um valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="a03bc-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="a03bc-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a03bc-115">EXAMPLES</span></span>

### <span data-ttu-id="a03bc-116">Exemplo 1: atualizar um módulo</span><span class="sxs-lookup"><span data-stu-id="a03bc-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a03bc-117">Esse comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a03bc-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="a03bc-118">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.</span><span class="sxs-lookup"><span data-stu-id="a03bc-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="a03bc-119">OS</span><span class="sxs-lookup"><span data-stu-id="a03bc-119">PARAMETERS</span></span>

### <span data-ttu-id="a03bc-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a03bc-120">-AutomationAccountName</span></span>
<span data-ttu-id="a03bc-121">Especifica o nome da conta de automação para a qual esse cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="a03bc-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="a03bc-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="a03bc-122">-ContentLinkUri</span></span>
<span data-ttu-id="a03bc-123">Especifica a URL do arquivo. zip que contém a nova versão de um módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="a03bc-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03bc-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="a03bc-124">-ContentLinkVersion</span></span>
<span data-ttu-id="a03bc-125">Especifica a versão do módulo para a qual esse cmdlet atualiza a automação.</span><span class="sxs-lookup"><span data-stu-id="a03bc-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03bc-126">-DefaultProfile</span></span>
<span data-ttu-id="a03bc-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a03bc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a03bc-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a03bc-128">-Name</span></span>
<span data-ttu-id="a03bc-129">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="a03bc-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="a03bc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03bc-130">-ResourceGroupName</span></span>
<span data-ttu-id="a03bc-131">Especifica o nome de um grupo de recursos para o qual esse cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="a03bc-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="a03bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03bc-132">CommonParameters</span></span>
<span data-ttu-id="a03bc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03bc-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03bc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03bc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a03bc-135">INPUTS</span></span>

### <span data-ttu-id="a03bc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a03bc-136">System.String</span></span>

### <span data-ttu-id="a03bc-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="a03bc-137">System.Uri</span></span>

## <span data-ttu-id="a03bc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a03bc-138">OUTPUTS</span></span>

### <span data-ttu-id="a03bc-139">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="a03bc-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="a03bc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a03bc-140">NOTES</span></span>

## <span data-ttu-id="a03bc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a03bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="a03bc-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a03bc-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="a03bc-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a03bc-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="a03bc-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a03bc-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


