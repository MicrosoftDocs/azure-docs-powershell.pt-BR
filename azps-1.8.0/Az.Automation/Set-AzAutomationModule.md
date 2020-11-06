---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: d9c036c7047ee0d568f5e1451bce46dfe2903e29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601503"
---
# <span data-ttu-id="7b72f-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b72f-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="7b72f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b72f-102">SYNOPSIS</span></span>
<span data-ttu-id="7b72f-103">Atualiza um módulo na automação.</span><span class="sxs-lookup"><span data-stu-id="7b72f-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="7b72f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b72f-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b72f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b72f-105">DESCRIPTION</span></span>
<span data-ttu-id="7b72f-106">O cmdlet **set-AzAutomationModule** atualiza um módulo na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b72f-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="7b72f-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="7b72f-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="7b72f-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="7b72f-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="7b72f-109">wps_2 módulo, que tem a extensão de nome de arquivo. psm1 ou. dll</span><span class="sxs-lookup"><span data-stu-id="7b72f-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="7b72f-110">wps_2 manifesto do módulo, que tem a extensão de nome de arquivo. psd1, o nome do arquivo. zip, o nome da pasta e o nome do arquivo na pasta devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="7b72f-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="7b72f-111">Especifique o arquivo. zip como uma URL que o serviço de automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="7b72f-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="7b72f-112">Se você importar um módulo wps_2 para a automação usando este cmdlet ou o cmdlet New-AzAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7b72f-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="7b72f-113">O comando termina se a importação tiver êxito ou falhará.</span><span class="sxs-lookup"><span data-stu-id="7b72f-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="7b72f-114">Para verificar se foi bem-sucedida, execute o seguinte comando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Verifique a propriedade **ProvisioningState** para obter um valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="7b72f-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="7b72f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b72f-115">EXAMPLES</span></span>

### <span data-ttu-id="7b72f-116">Exemplo 1: atualizar um módulo</span><span class="sxs-lookup"><span data-stu-id="7b72f-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7b72f-117">Esse comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7b72f-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="7b72f-118">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.</span><span class="sxs-lookup"><span data-stu-id="7b72f-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="7b72f-119">OS</span><span class="sxs-lookup"><span data-stu-id="7b72f-119">PARAMETERS</span></span>

### <span data-ttu-id="7b72f-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b72f-120">-AutomationAccountName</span></span>
<span data-ttu-id="7b72f-121">Especifica o nome da conta de automação para a qual esse cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="7b72f-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="7b72f-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="7b72f-122">-ContentLinkUri</span></span>
<span data-ttu-id="7b72f-123">Especifica a URL do arquivo. zip que contém a nova versão de um módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="7b72f-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7b72f-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="7b72f-124">-ContentLinkVersion</span></span>
<span data-ttu-id="7b72f-125">Especifica a versão do módulo para a qual esse cmdlet atualiza a automação.</span><span class="sxs-lookup"><span data-stu-id="7b72f-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="7b72f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b72f-126">-DefaultProfile</span></span>
<span data-ttu-id="7b72f-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7b72f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b72f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b72f-128">-Name</span></span>
<span data-ttu-id="7b72f-129">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="7b72f-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7b72f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b72f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7b72f-131">Especifica o nome de um grupo de recursos para o qual esse cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="7b72f-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="7b72f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b72f-132">CommonParameters</span></span>
<span data-ttu-id="7b72f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b72f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b72f-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b72f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b72f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b72f-135">INPUTS</span></span>

### <span data-ttu-id="7b72f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7b72f-136">System.String</span></span>

### <span data-ttu-id="7b72f-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="7b72f-137">System.Uri</span></span>

## <span data-ttu-id="7b72f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b72f-138">OUTPUTS</span></span>

### <span data-ttu-id="7b72f-139">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="7b72f-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="7b72f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b72f-140">NOTES</span></span>

## <span data-ttu-id="7b72f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b72f-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b72f-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b72f-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="7b72f-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b72f-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="7b72f-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b72f-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


