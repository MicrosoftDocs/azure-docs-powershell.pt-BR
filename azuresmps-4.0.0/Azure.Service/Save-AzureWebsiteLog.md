---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945458"
---
# <span data-ttu-id="16458-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="16458-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="16458-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16458-102">SYNOPSIS</span></span>
<span data-ttu-id="16458-103">Baixa e salva os logs para um site específico.</span><span class="sxs-lookup"><span data-stu-id="16458-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="16458-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16458-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="16458-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16458-105">DESCRIPTION</span></span>
<span data-ttu-id="16458-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16458-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="16458-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="16458-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="16458-108">O cmdlet **Save-AzureWebsiteLog** baixa os logs para um site específico.</span><span class="sxs-lookup"><span data-stu-id="16458-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="16458-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16458-109">EXAMPLES</span></span>

### <span data-ttu-id="16458-110">Exemplo 1: baixar e salvar logs para um site</span><span class="sxs-lookup"><span data-stu-id="16458-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="16458-111">Este exemplo baixa os logs de tempo de execução e implantação do site meusite para o arquivo logs.zip no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="16458-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="16458-112">OS</span><span class="sxs-lookup"><span data-stu-id="16458-112">PARAMETERS</span></span>

### <span data-ttu-id="16458-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="16458-113">-Name</span></span>
<span data-ttu-id="16458-114">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="16458-114">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16458-115">-Saída</span><span class="sxs-lookup"><span data-stu-id="16458-115">-Output</span></span>
<span data-ttu-id="16458-116">Especifica o caminho para armazenar o arquivo baixado.</span><span class="sxs-lookup"><span data-stu-id="16458-116">Specifies the path to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16458-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16458-117">-PassThru</span></span>
<span data-ttu-id="16458-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="16458-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16458-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="16458-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16458-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="16458-120">-Profile</span></span>
<span data-ttu-id="16458-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="16458-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16458-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="16458-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16458-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="16458-123">-Slot</span></span>
<span data-ttu-id="16458-124">Especifica o nome do slot.</span><span class="sxs-lookup"><span data-stu-id="16458-124">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16458-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16458-125">CommonParameters</span></span>
<span data-ttu-id="16458-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16458-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16458-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16458-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16458-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16458-128">INPUTS</span></span>

## <span data-ttu-id="16458-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16458-129">OUTPUTS</span></span>

## <span data-ttu-id="16458-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16458-130">NOTES</span></span>

## <span data-ttu-id="16458-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16458-131">RELATED LINKS</span></span>

[<span data-ttu-id="16458-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="16458-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


