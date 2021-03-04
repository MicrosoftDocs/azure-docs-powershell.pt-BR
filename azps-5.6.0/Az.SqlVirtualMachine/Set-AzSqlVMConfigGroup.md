---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: 4dd2042ae3c7e84b9a7a82dde19fb5848229f51c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887294"
---
# <span data-ttu-id="7bd4b-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="7bd4b-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="7bd4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd4b-103">De definir as informações relativas a um grupo de máquinas virtuais sql em uma configuração de máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="7bd4b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7bd4b-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd4b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bd4b-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd4b-106">O Set-AzSqlVMConfigGroup cmdlet definiu as informações necessárias para ingressar em um grupo de máquinas virtuais sql para uma configuração de máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="7bd4b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd4b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bd4b-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="7bd4b-109">Atualize as informações de grupo de uma configuração de máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="7bd4b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-110">PARAMETERS</span></span>

### <span data-ttu-id="7bd4b-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7bd4b-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="7bd4b-112">Senha para a conta bootstrap de cluster</span><span class="sxs-lookup"><span data-stu-id="7bd4b-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd4b-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7bd4b-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="7bd4b-114">Senha para a conta do operador de cluster</span><span class="sxs-lookup"><span data-stu-id="7bd4b-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd4b-115">-DefaultProfile</span></span>
<span data-ttu-id="7bd4b-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd4b-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7bd4b-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="7bd4b-118">Senha para a SQL de serviço</span><span class="sxs-lookup"><span data-stu-id="7bd4b-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd4b-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="7bd4b-119">-SqlVM</span></span>
<span data-ttu-id="7bd4b-120">A SQL configuração da máquina virtual à qual a associação de grupo será adicionada</span><span class="sxs-lookup"><span data-stu-id="7bd4b-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd4b-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="7bd4b-121">-SqlVMGroup</span></span>
<span data-ttu-id="7bd4b-122">O grupo do SQL virtual fará parte</span><span class="sxs-lookup"><span data-stu-id="7bd4b-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd4b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd4b-123">CommonParameters</span></span>
<span data-ttu-id="7bd4b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd4b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd4b-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd4b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd4b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-126">INPUTS</span></span>

### <span data-ttu-id="7bd4b-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7bd4b-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7bd4b-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-128">OUTPUTS</span></span>

### <span data-ttu-id="7bd4b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7bd4b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7bd4b-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="7bd4b-130">NOTES</span></span>

## <span data-ttu-id="7bd4b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bd4b-131">RELATED LINKS</span></span>
