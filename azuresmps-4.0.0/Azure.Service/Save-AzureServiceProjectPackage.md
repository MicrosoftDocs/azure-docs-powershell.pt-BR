---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945460"
---
# <span data-ttu-id="11799-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="11799-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="11799-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11799-102">SYNOPSIS</span></span>
<span data-ttu-id="11799-103">Empacota o projeto de serviço no pacote de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="11799-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="11799-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11799-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11799-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11799-105">DESCRIPTION</span></span>
<span data-ttu-id="11799-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="11799-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="11799-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="11799-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="11799-108">O cmdlet **Save-AzureServiceProjectPackage** empacota o projeto de serviço em um pacote de nuvem do Azure (\*. cspkg).</span><span class="sxs-lookup"><span data-stu-id="11799-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="11799-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11799-109">EXAMPLES</span></span>

### <span data-ttu-id="11799-110">Exemplo 1: criar um pacote de projeto de serviço</span><span class="sxs-lookup"><span data-stu-id="11799-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="11799-111">Este exemplo cria um \*. cspgk para um projeto de serviço chamado MyAzureServiceProject.</span><span class="sxs-lookup"><span data-stu-id="11799-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="11799-112">OS</span><span class="sxs-lookup"><span data-stu-id="11799-112">PARAMETERS</span></span>

### <span data-ttu-id="11799-113">-Local</span><span class="sxs-lookup"><span data-stu-id="11799-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11799-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="11799-114">-Profile</span></span>
<span data-ttu-id="11799-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="11799-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11799-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="11799-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11799-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11799-117">CommonParameters</span></span>
<span data-ttu-id="11799-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11799-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11799-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11799-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11799-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11799-120">INPUTS</span></span>

## <span data-ttu-id="11799-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11799-121">OUTPUTS</span></span>

## <span data-ttu-id="11799-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11799-122">NOTES</span></span>

## <span data-ttu-id="11799-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11799-123">RELATED LINKS</span></span>

[<span data-ttu-id="11799-124">Publicar-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="11799-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


