---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892880"
---
# <span data-ttu-id="1f725-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f725-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="1f725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f725-102">SYNOPSIS</span></span>
<span data-ttu-id="1f725-103">Atualiza um módulo em Automação.</span><span class="sxs-lookup"><span data-stu-id="1f725-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="1f725-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1f725-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f725-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1f725-105">DESCRIPTION</span></span>
<span data-ttu-id="1f725-106">O cmdlet **Set-AzAutomationModule** atualiza um módulo no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1f725-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="1f725-107">Este comando aceita um arquivo compactado que tem uma extensão de nome de arquivo .zip.</span><span class="sxs-lookup"><span data-stu-id="1f725-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="1f725-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="1f725-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="1f725-109">wps_2 módulo, que tem uma extensão de nome de arquivo .psm1 ou .dll</span><span class="sxs-lookup"><span data-stu-id="1f725-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="1f725-110">wps_2 de módulo, que tem uma extensão de nome de arquivo .psd1 O nome do arquivo .zip, o nome da pasta e o nome do arquivo na pasta devem ser os mesmos.</span><span class="sxs-lookup"><span data-stu-id="1f725-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="1f725-111">Especifique o arquivo .zip como uma URL que o serviço de Automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="1f725-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="1f725-112">Se você importar um wps_2 para Automação usando este cmdlet ou o cmdlet New-AzAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1f725-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="1f725-113">O comando termina se a importação é bem-sucedida ou falha.</span><span class="sxs-lookup"><span data-stu-id="1f725-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="1f725-114">Para verificar se foi bem-sucedido, execute o seguinte comando: ModuleName Verifique a propriedade `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` **ProvisioningState** para obter um valor de Succeeded.</span><span class="sxs-lookup"><span data-stu-id="1f725-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="1f725-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f725-115">EXAMPLES</span></span>

### <span data-ttu-id="1f725-116">Exemplo 1: atualizar um módulo</span><span class="sxs-lookup"><span data-stu-id="1f725-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1f725-117">Este comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de Automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1f725-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="1f725-118">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e em um contêiner denominado módulos.</span><span class="sxs-lookup"><span data-stu-id="1f725-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="1f725-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1f725-119">PARAMETERS</span></span>

### <span data-ttu-id="1f725-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f725-120">-AutomationAccountName</span></span>
<span data-ttu-id="1f725-121">Especifica o nome da conta de automação para a qual este cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="1f725-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="1f725-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="1f725-122">-ContentLinkUri</span></span>
<span data-ttu-id="1f725-123">Especifica a URL do arquivo .zip que contém a nova versão de um módulo que esse cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="1f725-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="1f725-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="1f725-124">-ContentLinkVersion</span></span>
<span data-ttu-id="1f725-125">Especifica a versão do módulo ao qual este cmdlet atualiza a Automação.</span><span class="sxs-lookup"><span data-stu-id="1f725-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="1f725-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f725-126">-DefaultProfile</span></span>
<span data-ttu-id="1f725-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1f725-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f725-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1f725-128">-Name</span></span>
<span data-ttu-id="1f725-129">Especifica o nome do módulo que esse cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="1f725-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="1f725-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f725-130">-ResourceGroupName</span></span>
<span data-ttu-id="1f725-131">Especifica o nome de um grupo de recursos para o qual este cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="1f725-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="1f725-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f725-132">CommonParameters</span></span>
<span data-ttu-id="1f725-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f725-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f725-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f725-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f725-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f725-135">INPUTS</span></span>

### <span data-ttu-id="1f725-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1f725-136">System.String</span></span>

### <span data-ttu-id="1f725-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="1f725-137">System.Uri</span></span>

## <span data-ttu-id="1f725-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1f725-138">OUTPUTS</span></span>

### <span data-ttu-id="1f725-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="1f725-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="1f725-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="1f725-140">NOTES</span></span>

## <span data-ttu-id="1f725-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f725-141">RELATED LINKS</span></span>

[<span data-ttu-id="1f725-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f725-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="1f725-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f725-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="1f725-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f725-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


