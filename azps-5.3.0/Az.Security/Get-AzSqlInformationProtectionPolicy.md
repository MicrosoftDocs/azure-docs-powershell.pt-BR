---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433262"
---
# <span data-ttu-id="d37f1-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d37f1-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="d37f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d37f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d37f1-103">Recupera a política de proteção de informações SQL do locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="d37f1-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="d37f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d37f1-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d37f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d37f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d37f1-106">Recupera a política de proteção de informações SQL do locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="d37f1-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="d37f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d37f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d37f1-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d37f1-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="d37f1-109">OS</span><span class="sxs-lookup"><span data-stu-id="d37f1-109">PARAMETERS</span></span>

### <span data-ttu-id="d37f1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d37f1-110">-AsJob</span></span>
<span data-ttu-id="d37f1-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d37f1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d37f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37f1-112">-DefaultProfile</span></span>
<span data-ttu-id="d37f1-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d37f1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37f1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37f1-114">CommonParameters</span></span>
<span data-ttu-id="d37f1-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37f1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37f1-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d37f1-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37f1-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d37f1-117">INPUTS</span></span>

### <span data-ttu-id="d37f1-118">System. String</span><span class="sxs-lookup"><span data-stu-id="d37f1-118">System.string</span></span>

## <span data-ttu-id="d37f1-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d37f1-119">OUTPUTS</span></span>

### <span data-ttu-id="d37f1-120">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d37f1-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="d37f1-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d37f1-121">NOTES</span></span>

## <span data-ttu-id="d37f1-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d37f1-122">RELATED LINKS</span></span>
