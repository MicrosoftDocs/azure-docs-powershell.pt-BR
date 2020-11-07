---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946389"
---
# <span data-ttu-id="af065-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="af065-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="af065-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af065-102">SYNOPSIS</span></span>
<span data-ttu-id="af065-103">Cria os arquivos e pastas necessários para que um aplicativo Node.js seja hospedado na nuvem via node.exe</span><span class="sxs-lookup"><span data-stu-id="af065-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="af065-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af065-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="af065-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af065-105">DESCRIPTION</span></span>
<span data-ttu-id="af065-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="af065-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="af065-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="af065-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="af065-108">O cmdlet **Add-AzureNodeWorkerRole** cria os arquivos e as pastas necessárias, às vezes chamados de scaffolding, para que um aplicativo Node.js seja hospedado na nuvem via node.exe.</span><span class="sxs-lookup"><span data-stu-id="af065-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="af065-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af065-109">EXAMPLES</span></span>

### <span data-ttu-id="af065-110">Exemplo 1: função de trabalho de instância única</span><span class="sxs-lookup"><span data-stu-id="af065-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="af065-111">Este exemplo adiciona scaffolding para uma única função de trabalho chamada **MyWorkerRole** ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="af065-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="af065-112">Exemplo 2: função de trabalho de várias instâncias</span><span class="sxs-lookup"><span data-stu-id="af065-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="af065-113">Este exemplo adiciona scaffolding para uma única função de trabalho chamada **MyWorkerRole** ao aplicativo atual, com uma contagem de instância de função 2.</span><span class="sxs-lookup"><span data-stu-id="af065-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="af065-114">OS</span><span class="sxs-lookup"><span data-stu-id="af065-114">PARAMETERS</span></span>

### <span data-ttu-id="af065-115">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="af065-115">-Instances</span></span>
<span data-ttu-id="af065-116">Especifica o número de instâncias de função para esta função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="af065-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="af065-117">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="af065-117">Default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af065-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="af065-118">-Name</span></span>
<span data-ttu-id="af065-119">Especifica o nome da função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="af065-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="af065-120">O valor determina o nome da pasta que contém o scaffolding para o serviço de node.js hospedado na função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="af065-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="af065-121">O padrão é WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="af065-121">Default is WorkerRole1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af065-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="af065-122">-Profile</span></span>
<span data-ttu-id="af065-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="af065-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af065-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="af065-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af065-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af065-125">CommonParameters</span></span>
<span data-ttu-id="af065-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af065-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af065-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af065-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af065-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af065-128">INPUTS</span></span>

## <span data-ttu-id="af065-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af065-129">OUTPUTS</span></span>

## <span data-ttu-id="af065-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af065-130">NOTES</span></span>

## <span data-ttu-id="af065-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af065-131">RELATED LINKS</span></span>

[<span data-ttu-id="af065-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="af065-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="af065-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="af065-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


