---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946218"
---
# <span data-ttu-id="a643b-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a643b-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="a643b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a643b-102">SYNOPSIS</span></span>
<span data-ttu-id="a643b-103">Cria os arquivos e a configuração necessários para um novo serviço.</span><span class="sxs-lookup"><span data-stu-id="a643b-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="a643b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a643b-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a643b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a643b-105">DESCRIPTION</span></span>
<span data-ttu-id="a643b-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a643b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a643b-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a643b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a643b-108">O cmdlet **New-AzureServiceProject** cria os arquivos e a configuração necessários para um novo serviço do Azure no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="a643b-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="a643b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a643b-109">EXAMPLES</span></span>

### <span data-ttu-id="a643b-110">Exemplo 1: criar scaffolding para um serviço</span><span class="sxs-lookup"><span data-stu-id="a643b-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="a643b-111">Este exemplo cria scaffolding para um novo serviço do Azure chamado MyService1 no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="a643b-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="a643b-112">OS</span><span class="sxs-lookup"><span data-stu-id="a643b-112">PARAMETERS</span></span>

### <span data-ttu-id="a643b-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a643b-113">-Profile</span></span>
<span data-ttu-id="a643b-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a643b-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a643b-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a643b-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a643b-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a643b-116">-ServiceName</span></span>
<span data-ttu-id="a643b-117">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a643b-117">Specifies the name of the service.</span></span>
<span data-ttu-id="a643b-118">Ele determina a primeira seção do nome do host do serviço (por exemplo, name.cloudapp.net) e o diretório que conterá o serviço.</span><span class="sxs-lookup"><span data-stu-id="a643b-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="a643b-119">O nome pode conter apenas letras, dígitos e o caractere traço (-).</span><span class="sxs-lookup"><span data-stu-id="a643b-119">The name can contain only letters, digits, and the dash character (-).</span></span>

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

### <span data-ttu-id="a643b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a643b-120">CommonParameters</span></span>
<span data-ttu-id="a643b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a643b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a643b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a643b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a643b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a643b-123">INPUTS</span></span>

## <span data-ttu-id="a643b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a643b-124">OUTPUTS</span></span>

## <span data-ttu-id="a643b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a643b-125">NOTES</span></span>

## <span data-ttu-id="a643b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a643b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a643b-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="a643b-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="a643b-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="a643b-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="a643b-129">Publicar-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a643b-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="a643b-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a643b-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="a643b-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="a643b-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


