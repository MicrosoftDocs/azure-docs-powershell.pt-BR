---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946223"
---
# <span data-ttu-id="644e5-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644e5-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="644e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="644e5-102">SYNOPSIS</span></span>

<span data-ttu-id="644e5-103">Importa um módulo para a automação.</span><span class="sxs-lookup"><span data-stu-id="644e5-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="644e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="644e5-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="644e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="644e5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="644e5-106">O cmdlet **New-AzureAutomationModule** importa um módulo para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="644e5-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="644e5-107">Um módulo é um arquivo compactado com uma extensão. zip, que contém uma pasta que inclui um dos seguintes tipos de arquivo:</span><span class="sxs-lookup"><span data-stu-id="644e5-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="644e5-108">Um módulo do Windows PowerShell (arquivo psm1).</span><span class="sxs-lookup"><span data-stu-id="644e5-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="644e5-109">Um manifesto do módulo do Windows PowerShell (arquivo psd1).</span><span class="sxs-lookup"><span data-stu-id="644e5-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="644e5-110">Um assembly (arquivo dll).</span><span class="sxs-lookup"><span data-stu-id="644e5-110">An assembly (dll file).</span></span>

<span data-ttu-id="644e5-111">Os nomes do arquivo zip, a pasta no arquivo zip e o arquivo na pasta (. psm1, PSD. 1 ou. dll) devem coincidir.</span><span class="sxs-lookup"><span data-stu-id="644e5-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="644e5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="644e5-112">EXAMPLES</span></span>

### <span data-ttu-id="644e5-113">Exemplo 1: importar um módulo</span><span class="sxs-lookup"><span data-stu-id="644e5-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="644e5-114">Esse comando importa um módulo chamado ContosoModule para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="644e5-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="644e5-115">O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.</span><span class="sxs-lookup"><span data-stu-id="644e5-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="644e5-116">OS</span><span class="sxs-lookup"><span data-stu-id="644e5-116">PARAMETERS</span></span>

### <span data-ttu-id="644e5-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="644e5-117">-AutomationAccountName</span></span>
<span data-ttu-id="644e5-118">Especifica o nome da conta de automação na qual o módulo será armazenado.</span><span class="sxs-lookup"><span data-stu-id="644e5-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644e5-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="644e5-119">-ContentLink</span></span>
<span data-ttu-id="644e5-120">URL pública, como um site ou um armazenamento de blob do Azure que especifica o caminho para o arquivo de módulo.</span><span class="sxs-lookup"><span data-stu-id="644e5-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="644e5-121">Este local deve ser acessível publicamente.</span><span class="sxs-lookup"><span data-stu-id="644e5-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644e5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="644e5-122">-Name</span></span>
<span data-ttu-id="644e5-123">Especifica um nome para o módulo.</span><span class="sxs-lookup"><span data-stu-id="644e5-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644e5-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="644e5-124">-Profile</span></span>
<span data-ttu-id="644e5-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="644e5-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="644e5-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="644e5-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644e5-127">-Marcas</span><span class="sxs-lookup"><span data-stu-id="644e5-127">-Tags</span></span>
<span data-ttu-id="644e5-128">Especifica uma ou mais marcas relacionadas ao módulo.</span><span class="sxs-lookup"><span data-stu-id="644e5-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644e5-129">CommonParameters</span></span>
<span data-ttu-id="644e5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="644e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644e5-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644e5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644e5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="644e5-132">INPUTS</span></span>

## <span data-ttu-id="644e5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="644e5-133">OUTPUTS</span></span>

### <span data-ttu-id="644e5-134">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="644e5-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="644e5-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="644e5-135">NOTES</span></span>

## <span data-ttu-id="644e5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="644e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="644e5-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644e5-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="644e5-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644e5-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="644e5-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644e5-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


