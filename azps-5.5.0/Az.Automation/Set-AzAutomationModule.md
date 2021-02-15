---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112251"
---
# <span data-ttu-id="ccedb-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ccedb-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="ccedb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccedb-102">SYNOPSIS</span></span>
<span data-ttu-id="ccedb-103">Atualiza um módulo em Automação.</span><span class="sxs-lookup"><span data-stu-id="ccedb-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="ccedb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccedb-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccedb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccedb-105">DESCRIPTION</span></span>
<span data-ttu-id="ccedb-106">O cmdlet **Set-AzAutomationModule** atualiza um módulo na Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccedb-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="ccedb-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo .zip.</span><span class="sxs-lookup"><span data-stu-id="ccedb-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="ccedb-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="ccedb-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="ccedb-109">wps_2 módulo, que tem uma extensão de nome de arquivo .psm1 ou .dll</span><span class="sxs-lookup"><span data-stu-id="ccedb-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="ccedb-110">wps_2 de módulo, que tem uma extensão de nome de arquivo .psd1, o nome do arquivo .zip, o nome da pasta e o nome do arquivo na pasta devem ser os mesmos.</span><span class="sxs-lookup"><span data-stu-id="ccedb-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="ccedb-111">Especifique o arquivo .zip como uma URL que o serviço automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="ccedb-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="ccedb-112">Se você importar um módulo wps_2 para Automação usando este cmdlet ou o cmdlet New-AzAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ccedb-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="ccedb-113">O comando termina se a importação é bem-sucedida ou falha.</span><span class="sxs-lookup"><span data-stu-id="ccedb-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="ccedb-114">Para verificar se ele foi bem-sucedido, execute o seguinte comando: ModuleName Verifique a propriedade `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` **ProvisioningState** para obter um valor de Bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ccedb-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="ccedb-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccedb-115">EXAMPLES</span></span>

### <span data-ttu-id="ccedb-116">Exemplo 1: Atualizar um módulo</span><span class="sxs-lookup"><span data-stu-id="ccedb-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ccedb-117">Esse comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de Automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ccedb-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="ccedb-118">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e em um contêiner denominado módulos.</span><span class="sxs-lookup"><span data-stu-id="ccedb-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="ccedb-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccedb-119">PARAMETERS</span></span>

### <span data-ttu-id="ccedb-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ccedb-120">-AutomationAccountName</span></span>
<span data-ttu-id="ccedb-121">Especifica o nome da conta automação para a qual este cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="ccedb-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="ccedb-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="ccedb-122">-ContentLinkUri</span></span>
<span data-ttu-id="ccedb-123">Especifica a URL do arquivo .zip que contém a nova versão de um módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="ccedb-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="ccedb-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="ccedb-124">-ContentLinkVersion</span></span>
<span data-ttu-id="ccedb-125">Especifica a versão do módulo ao qual este cmdlet atualiza Automação.</span><span class="sxs-lookup"><span data-stu-id="ccedb-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="ccedb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccedb-126">-DefaultProfile</span></span>
<span data-ttu-id="ccedb-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ccedb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccedb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccedb-128">-Name</span></span>
<span data-ttu-id="ccedb-129">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="ccedb-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="ccedb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccedb-130">-ResourceGroupName</span></span>
<span data-ttu-id="ccedb-131">Especifica o nome de um grupo de recursos para o qual este cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="ccedb-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="ccedb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccedb-132">CommonParameters</span></span>
<span data-ttu-id="ccedb-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccedb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccedb-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccedb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccedb-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="ccedb-135">INPUTS</span></span>

### <span data-ttu-id="ccedb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ccedb-136">System.String</span></span>

### <span data-ttu-id="ccedb-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="ccedb-137">System.Uri</span></span>

## <span data-ttu-id="ccedb-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ccedb-138">OUTPUTS</span></span>

### <span data-ttu-id="ccedb-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="ccedb-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="ccedb-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ccedb-140">NOTES</span></span>

## <span data-ttu-id="ccedb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccedb-141">RELATED LINKS</span></span>

[<span data-ttu-id="ccedb-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ccedb-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="ccedb-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ccedb-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="ccedb-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ccedb-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


