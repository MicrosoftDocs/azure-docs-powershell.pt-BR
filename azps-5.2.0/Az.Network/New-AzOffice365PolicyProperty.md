---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257612"
---
# <span data-ttu-id="1b93c-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="1b93c-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="1b93c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b93c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b93c-103">Defina uma nova política de debates do tráfego do Office 365 para ser usada com um site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="1b93c-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="1b93c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b93c-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b93c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b93c-105">DESCRIPTION</span></span>
<span data-ttu-id="1b93c-106">O comando New-AzOffice365PolicyProperties define uma política de debate do Office 365 que deve ser usada com um site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="1b93c-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="1b93c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b93c-107">EXAMPLES</span></span>

### <span data-ttu-id="1b93c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b93c-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="1b93c-109">Crie o objeto da política de debates do tráfego do Office 365 para ser usado com comandos do site do Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="1b93c-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="1b93c-110">OS</span><span class="sxs-lookup"><span data-stu-id="1b93c-110">PARAMETERS</span></span>

### <span data-ttu-id="1b93c-111">-Permitir</span><span class="sxs-lookup"><span data-stu-id="1b93c-111">-Allow</span></span>
<span data-ttu-id="1b93c-112">Debate o tráfego permitir categoria.</span><span class="sxs-lookup"><span data-stu-id="1b93c-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b93c-113">-Padrão</span><span class="sxs-lookup"><span data-stu-id="1b93c-113">-Default</span></span>
<span data-ttu-id="1b93c-114">Debate do tráfego de categoria padrão.</span><span class="sxs-lookup"><span data-stu-id="1b93c-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b93c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b93c-115">-DefaultProfile</span></span>
<span data-ttu-id="1b93c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b93c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b93c-117">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="1b93c-117">-Optimize</span></span>
<span data-ttu-id="1b93c-118">Debates sobre o tráfego de otimização da categoria.</span><span class="sxs-lookup"><span data-stu-id="1b93c-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b93c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b93c-119">CommonParameters</span></span>
<span data-ttu-id="1b93c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b93c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b93c-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b93c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b93c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b93c-122">INPUTS</span></span>

### <span data-ttu-id="1b93c-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1b93c-123">None</span></span>

## <span data-ttu-id="1b93c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b93c-124">OUTPUTS</span></span>

### <span data-ttu-id="1b93c-125">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="1b93c-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="1b93c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b93c-126">NOTES</span></span>

## <span data-ttu-id="1b93c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b93c-127">RELATED LINKS</span></span>
