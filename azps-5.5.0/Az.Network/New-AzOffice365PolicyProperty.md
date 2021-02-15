---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115115"
---
# <span data-ttu-id="63995-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="63995-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="63995-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63995-102">SYNOPSIS</span></span>
<span data-ttu-id="63995-103">Defina uma nova política de quebra de tráfego do Office 365 a ser usada com um site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="63995-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="63995-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63995-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63995-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="63995-105">DESCRIPTION</span></span>
<span data-ttu-id="63995-106">O New-AzOffice365PolicyProperties define uma política de saída do Office 365 que deve ser usada com um site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="63995-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="63995-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63995-107">EXAMPLES</span></span>

### <span data-ttu-id="63995-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63995-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="63995-109">Crie um objeto de política de política de quebra de tráfego do Office 365 para ser usado com comandos de site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="63995-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="63995-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63995-110">PARAMETERS</span></span>

### <span data-ttu-id="63995-111">-Permitir</span><span class="sxs-lookup"><span data-stu-id="63995-111">-Allow</span></span>
<span data-ttu-id="63995-112">Desafore o tráfego de categoria de permitir.</span><span class="sxs-lookup"><span data-stu-id="63995-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="63995-113">-Padrão</span><span class="sxs-lookup"><span data-stu-id="63995-113">-Default</span></span>
<span data-ttu-id="63995-114">Separar o tráfego de categoria padrão.</span><span class="sxs-lookup"><span data-stu-id="63995-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="63995-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63995-115">-DefaultProfile</span></span>
<span data-ttu-id="63995-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63995-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63995-117">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="63995-117">-Optimize</span></span>
<span data-ttu-id="63995-118">Desembre o tráfego de categoria otimizado.</span><span class="sxs-lookup"><span data-stu-id="63995-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="63995-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63995-119">CommonParameters</span></span>
<span data-ttu-id="63995-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63995-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63995-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63995-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63995-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="63995-122">INPUTS</span></span>

### <span data-ttu-id="63995-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="63995-123">None</span></span>

## <span data-ttu-id="63995-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="63995-124">OUTPUTS</span></span>

### <span data-ttu-id="63995-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="63995-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="63995-126">Notas</span><span class="sxs-lookup"><span data-stu-id="63995-126">NOTES</span></span>

## <span data-ttu-id="63995-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63995-127">RELATED LINKS</span></span>
