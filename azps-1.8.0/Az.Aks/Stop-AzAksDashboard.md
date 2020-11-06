---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595742"
---
# <span data-ttu-id="11418-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="11418-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="11418-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11418-102">SYNOPSIS</span></span>
<span data-ttu-id="11418-103">Interrompa o encapsulamento SSH Kubectl criado em Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="11418-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="11418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11418-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11418-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11418-105">DESCRIPTION</span></span>
<span data-ttu-id="11418-106">Interrompa o encapsulamento SSH Kubectl criado em Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="11418-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="11418-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11418-107">EXAMPLES</span></span>

### <span data-ttu-id="11418-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11418-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="11418-109">Interrompe a configuração existente do túnel SSH executando Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="11418-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="11418-110">OS</span><span class="sxs-lookup"><span data-stu-id="11418-110">PARAMETERS</span></span>

### <span data-ttu-id="11418-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11418-111">-DefaultProfile</span></span>
<span data-ttu-id="11418-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11418-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11418-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11418-113">-PassThru</span></span>
<span data-ttu-id="11418-114">Retorna verdadeiro se o encapsulamento SSH estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="11418-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="11418-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11418-115">CommonParameters</span></span>
<span data-ttu-id="11418-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11418-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11418-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11418-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11418-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11418-118">INPUTS</span></span>

### <span data-ttu-id="11418-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="11418-119">None</span></span>

## <span data-ttu-id="11418-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11418-120">OUTPUTS</span></span>

### <span data-ttu-id="11418-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11418-121">System.Boolean</span></span>

## <span data-ttu-id="11418-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11418-122">NOTES</span></span>

## <span data-ttu-id="11418-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11418-123">RELATED LINKS</span></span>
