---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428297"
---
# <span data-ttu-id="cb685-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb685-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="cb685-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb685-102">SYNOPSIS</span></span>
<span data-ttu-id="cb685-103">Atualiza um módulo na automação.</span><span class="sxs-lookup"><span data-stu-id="cb685-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb685-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb685-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb685-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb685-105">DESCRIPTION</span></span>
<span data-ttu-id="cb685-106">O cmdlet **set-AzureRmAutomationModule** atualiza um módulo na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb685-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="cb685-107">Esse comando aceita um arquivo compactado que tem uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="cb685-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="cb685-108">O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="cb685-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="cb685-109">wps_2 módulo, que tem a extensão de nome de arquivo. psm1 ou. dll</span><span class="sxs-lookup"><span data-stu-id="cb685-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="cb685-110">manifesto do módulo wps_2, que tem uma extensão de nome de arquivo. psd1</span><span class="sxs-lookup"><span data-stu-id="cb685-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="cb685-111">O nome do arquivo. zip, o nome da pasta e o nome do arquivo na pasta devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="cb685-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="cb685-112">Especifique o arquivo. zip como uma URL que o serviço de automação pode acessar.</span><span class="sxs-lookup"><span data-stu-id="cb685-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="cb685-113">Se você importar um módulo wps_2 para a automação usando este cmdlet ou o cmdlet New-AzureRmAutomationModule, a operação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="cb685-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="cb685-114">O comando termina se a importação tiver êxito ou falhará.</span><span class="sxs-lookup"><span data-stu-id="cb685-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="cb685-115">Para verificar se foi bem-sucedida, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="cb685-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="cb685-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="cb685-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="cb685-117">Verifique se a propriedade **ProvisioningState** tem um valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="cb685-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="cb685-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb685-118">EXAMPLES</span></span>

### <span data-ttu-id="cb685-119">Exemplo 1: atualizar um módulo</span><span class="sxs-lookup"><span data-stu-id="cb685-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cb685-120">Esse comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cb685-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cb685-121">OS</span><span class="sxs-lookup"><span data-stu-id="cb685-121">PARAMETERS</span></span>

### <span data-ttu-id="cb685-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb685-122">-AutomationAccountName</span></span>
<span data-ttu-id="cb685-123">Especifica o nome da conta de automação para a qual esse cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="cb685-123">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="cb685-124">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="cb685-124">-ContentLinkUri</span></span>
<span data-ttu-id="cb685-125">Especifica a URL do arquivo. zip que contém a nova versão de um módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="cb685-125">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="cb685-126">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="cb685-126">-ContentLinkVersion</span></span>
<span data-ttu-id="cb685-127">Especifica a versão do módulo para a qual esse cmdlet atualiza a automação.</span><span class="sxs-lookup"><span data-stu-id="cb685-127">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="cb685-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb685-128">-Name</span></span>
<span data-ttu-id="cb685-129">Especifica o nome do módulo que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="cb685-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="cb685-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb685-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb685-131">Especifica o nome de um grupo de recursos para o qual esse cmdlet atualiza um módulo.</span><span class="sxs-lookup"><span data-stu-id="cb685-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="cb685-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb685-132">-DefaultProfile</span></span>
<span data-ttu-id="cb685-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb685-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb685-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb685-134">CommonParameters</span></span>
<span data-ttu-id="cb685-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb685-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb685-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb685-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb685-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb685-137">INPUTS</span></span>

## <span data-ttu-id="cb685-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb685-138">OUTPUTS</span></span>

### <span data-ttu-id="cb685-139">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="cb685-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="cb685-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb685-140">NOTES</span></span>

## <span data-ttu-id="cb685-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb685-141">RELATED LINKS</span></span>

[<span data-ttu-id="cb685-142">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb685-142">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="cb685-143">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb685-143">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="cb685-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb685-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


