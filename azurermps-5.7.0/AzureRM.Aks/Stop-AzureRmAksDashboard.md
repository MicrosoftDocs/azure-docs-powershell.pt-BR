---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 4ec1c8c2788469ffd377127bc58f657c817434a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432525"
---
# <span data-ttu-id="22879-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="22879-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="22879-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22879-102">SYNOPSIS</span></span>
<span data-ttu-id="22879-103">Interrompa o encapsulamento SSH Kubectl criado em Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="22879-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22879-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22879-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22879-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22879-105">DESCRIPTION</span></span>
<span data-ttu-id="22879-106">Interrompa o encapsulamento SSH Kubectl criado em Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="22879-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="22879-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22879-107">EXAMPLES</span></span>

### <span data-ttu-id="22879-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22879-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="22879-109">Interrompe a configuração existente do túnel SSH executando Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="22879-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="22879-110">OS</span><span class="sxs-lookup"><span data-stu-id="22879-110">PARAMETERS</span></span>

### <span data-ttu-id="22879-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22879-111">-DefaultProfile</span></span>
<span data-ttu-id="22879-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22879-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22879-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22879-113">-PassThru</span></span>
<span data-ttu-id="22879-114">Retorna verdadeiro se o encapsulamento SSH estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="22879-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="22879-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22879-115">CommonParameters</span></span>
<span data-ttu-id="22879-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22879-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22879-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22879-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22879-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22879-118">INPUTS</span></span>

### <span data-ttu-id="22879-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="22879-119">None</span></span>

## <span data-ttu-id="22879-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22879-120">OUTPUTS</span></span>

### <span data-ttu-id="22879-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22879-121">System.Boolean</span></span>

## <span data-ttu-id="22879-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22879-122">NOTES</span></span>

## <span data-ttu-id="22879-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22879-123">RELATED LINKS</span></span>
