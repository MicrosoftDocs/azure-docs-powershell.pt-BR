---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946387"
---
# <span data-ttu-id="743d1-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="743d1-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="743d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="743d1-102">SYNOPSIS</span></span>
<span data-ttu-id="743d1-103">Cria os arquivos e a configuração necessários para um aplicativo PHP que será hospedado no Azure por meio de php.exe.</span><span class="sxs-lookup"><span data-stu-id="743d1-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="743d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="743d1-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="743d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="743d1-105">DESCRIPTION</span></span>
<span data-ttu-id="743d1-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="743d1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="743d1-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="743d1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="743d1-108">Cria os arquivos e a configuração necessários, às vezes chamados de scaffolding, para um aplicativo PHP que será hospedado no Azure por meio de php.exe.</span><span class="sxs-lookup"><span data-stu-id="743d1-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="743d1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="743d1-109">EXAMPLES</span></span>

### <span data-ttu-id="743d1-110">Exemplo 1: criar uma função de trabalho com uma única instância</span><span class="sxs-lookup"><span data-stu-id="743d1-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="743d1-111">Este exemplo adiciona os arquivos e a configuração necessários para uma única função de trabalho chamada MyWorkerRole ao aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="743d1-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="743d1-112">Exemplo 2: criar uma função de trabalho com várias instâncias</span><span class="sxs-lookup"><span data-stu-id="743d1-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="743d1-113">Este exemplo adiciona os arquivos e a configuração necessários para uma nova função de trabalho ao aplicativo atual, usando o nome MyWorkerRole com uma contagem de instâncias de função 2.</span><span class="sxs-lookup"><span data-stu-id="743d1-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="743d1-114">OS</span><span class="sxs-lookup"><span data-stu-id="743d1-114">PARAMETERS</span></span>

### <span data-ttu-id="743d1-115">-Instâncias</span><span class="sxs-lookup"><span data-stu-id="743d1-115">-Instances</span></span>
<span data-ttu-id="743d1-116">Especifica o número de instâncias de função para esta função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="743d1-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="743d1-117">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="743d1-117">The default is 1.</span></span>

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

### <span data-ttu-id="743d1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="743d1-118">-Name</span></span>
<span data-ttu-id="743d1-119">Especifica o nome da função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="743d1-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="743d1-120">O nome determina o nome da pasta que contém os arquivos necessários e a configuração para o serviço PHP hospedado na função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="743d1-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="743d1-121">O padrão é WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="743d1-121">The default is WorkerRole1.</span></span>

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

### <span data-ttu-id="743d1-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="743d1-122">-Profile</span></span>
<span data-ttu-id="743d1-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="743d1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="743d1-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="743d1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="743d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743d1-125">CommonParameters</span></span>
<span data-ttu-id="743d1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743d1-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743d1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="743d1-128">INPUTS</span></span>

## <span data-ttu-id="743d1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="743d1-129">OUTPUTS</span></span>

## <span data-ttu-id="743d1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="743d1-130">NOTES</span></span>

## <span data-ttu-id="743d1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="743d1-131">RELATED LINKS</span></span>

[<span data-ttu-id="743d1-132">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="743d1-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="743d1-133">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="743d1-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


