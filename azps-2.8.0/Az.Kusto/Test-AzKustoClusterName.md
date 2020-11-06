---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596104"
---
# <span data-ttu-id="25bf3-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="25bf3-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="25bf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="25bf3-103">Verifique se um determinado nome de cluster Kusto está disponível.</span><span class="sxs-lookup"><span data-stu-id="25bf3-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="25bf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25bf3-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25bf3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="25bf3-106">Verifique se um determinado nome de cluster Kusto está disponível.</span><span class="sxs-lookup"><span data-stu-id="25bf3-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="25bf3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="25bf3-108">Exemplo 1-Verifique a disponibilidade de um nome de cluster Kusto que está em uso</span><span class="sxs-lookup"><span data-stu-id="25bf3-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="25bf3-109">O comando acima retorna se um cluster Kusto chamado "mykustocluster" existe na região "central EUA".</span><span class="sxs-lookup"><span data-stu-id="25bf3-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="25bf3-110">Exemplo 2-Verifique a disponibilidade de um nome de cluster Kusto que não está em uso</span><span class="sxs-lookup"><span data-stu-id="25bf3-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="25bf3-111">O comando acima retorna se um cluster Kusto chamado "mykustocluster" existe na região "central EUA".</span><span class="sxs-lookup"><span data-stu-id="25bf3-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="25bf3-112">OS</span><span class="sxs-lookup"><span data-stu-id="25bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="25bf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bf3-113">-DefaultProfile</span></span>
<span data-ttu-id="25bf3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25bf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bf3-115">-Local</span><span class="sxs-lookup"><span data-stu-id="25bf3-115">-Location</span></span>
<span data-ttu-id="25bf3-116">O local onde deseja fazer a verificação.</span><span class="sxs-lookup"><span data-stu-id="25bf3-116">The location where to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bf3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="25bf3-117">-Name</span></span>
<span data-ttu-id="25bf3-118">Nome de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="25bf3-118">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bf3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bf3-119">CommonParameters</span></span>
<span data-ttu-id="25bf3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bf3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bf3-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bf3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bf3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25bf3-122">INPUTS</span></span>

### <span data-ttu-id="25bf3-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="25bf3-123">None</span></span>

## <span data-ttu-id="25bf3-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25bf3-124">OUTPUTS</span></span>

### <span data-ttu-id="25bf3-125">Microsoft. Azure. Commands. Kusto. Models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="25bf3-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="25bf3-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25bf3-126">NOTES</span></span>

## <span data-ttu-id="25bf3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25bf3-127">RELATED LINKS</span></span>
