---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945696"
---
# <span data-ttu-id="286fa-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="286fa-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="286fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="286fa-102">SYNOPSIS</span></span>
<span data-ttu-id="286fa-103">Desabilita o acesso à área de trabalho remota a um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="286fa-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="286fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="286fa-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="286fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="286fa-105">DESCRIPTION</span></span>
<span data-ttu-id="286fa-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="286fa-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="286fa-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="286fa-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="286fa-108">O **Disable-AzureServiceProjectRemoteDesktop** desabilita o acesso à área de trabalho remota a um serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="286fa-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="286fa-109">Você deve publicar o serviço usando o cmdlet **Publish-AzureServiceProject** após desabilitar o acesso à área de trabalho remota para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="286fa-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="286fa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="286fa-110">EXAMPLES</span></span>

## <span data-ttu-id="286fa-111">OS</span><span class="sxs-lookup"><span data-stu-id="286fa-111">PARAMETERS</span></span>

### <span data-ttu-id="286fa-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="286fa-112">-PassThru</span></span>
<span data-ttu-id="286fa-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="286fa-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="286fa-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="286fa-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="286fa-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="286fa-115">-Profile</span></span>
<span data-ttu-id="286fa-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="286fa-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="286fa-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="286fa-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="286fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286fa-118">CommonParameters</span></span>
<span data-ttu-id="286fa-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286fa-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286fa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286fa-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="286fa-121">INPUTS</span></span>

## <span data-ttu-id="286fa-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="286fa-122">OUTPUTS</span></span>

## <span data-ttu-id="286fa-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="286fa-123">NOTES</span></span>

## <span data-ttu-id="286fa-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="286fa-124">RELATED LINKS</span></span>

[<span data-ttu-id="286fa-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="286fa-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


