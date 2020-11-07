---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945598"
---
# <span data-ttu-id="7f211-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="7f211-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="7f211-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f211-102">SYNOPSIS</span></span>
<span data-ttu-id="7f211-103">Obtenha os runtimes disponíveis para instalar em uma função.</span><span class="sxs-lookup"><span data-stu-id="7f211-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="7f211-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f211-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f211-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f211-105">DESCRIPTION</span></span>
<span data-ttu-id="7f211-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7f211-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7f211-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7f211-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7f211-108">Obtém os tempos de execução disponíveis para instalar em uma função.</span><span class="sxs-lookup"><span data-stu-id="7f211-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="7f211-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f211-109">EXAMPLES</span></span>

## <span data-ttu-id="7f211-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f211-110">PARAMETERS</span></span>

### <span data-ttu-id="7f211-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7f211-111">-Profile</span></span>
<span data-ttu-id="7f211-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7f211-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f211-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7f211-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f211-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="7f211-114">-Runtime</span></span>
<span data-ttu-id="7f211-115">O nome do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7f211-115">The name of the runtime.</span></span>
<span data-ttu-id="7f211-116">Se um tempo de execução especificado, somente as versões específicas desse tempo de execução disponíveis para instalar em sua função no Windows Azure serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="7f211-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="7f211-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f211-117">CommonParameters</span></span>
<span data-ttu-id="7f211-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f211-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f211-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f211-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f211-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f211-120">INPUTS</span></span>

## <span data-ttu-id="7f211-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f211-121">OUTPUTS</span></span>

## <span data-ttu-id="7f211-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f211-122">NOTES</span></span>

## <span data-ttu-id="7f211-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f211-123">RELATED LINKS</span></span>

[<span data-ttu-id="7f211-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="7f211-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="7f211-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="7f211-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="7f211-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="7f211-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="7f211-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7f211-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


