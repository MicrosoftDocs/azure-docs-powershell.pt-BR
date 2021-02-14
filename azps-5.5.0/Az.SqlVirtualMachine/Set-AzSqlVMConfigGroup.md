---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110890"
---
# <span data-ttu-id="eaa68-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="eaa68-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="eaa68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eaa68-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa68-103">De definir as informações relativas a um grupo de máquinas virtuais sql em uma configuração de computador virtual sql.</span><span class="sxs-lookup"><span data-stu-id="eaa68-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="eaa68-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaa68-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eaa68-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eaa68-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa68-106">O Set-AzSqlVMConfigGroup cmdlet definiu as informações necessárias para ingressar em um grupo de máquinas virtuais sql para uma configuração de computador virtual sql.</span><span class="sxs-lookup"><span data-stu-id="eaa68-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="eaa68-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eaa68-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa68-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eaa68-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="eaa68-109">Atualize as informações de grupo de uma configuração de computador virtual sql.</span><span class="sxs-lookup"><span data-stu-id="eaa68-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="eaa68-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaa68-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa68-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="eaa68-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="eaa68-112">Senha da conta bootstrap de cluster</span><span class="sxs-lookup"><span data-stu-id="eaa68-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="eaa68-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="eaa68-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="eaa68-114">Senha da conta do operador de cluster</span><span class="sxs-lookup"><span data-stu-id="eaa68-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="eaa68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa68-115">-DefaultProfile</span></span>
<span data-ttu-id="eaa68-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaa68-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="eaa68-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="eaa68-118">Senha da conta de serviço SQL</span><span class="sxs-lookup"><span data-stu-id="eaa68-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="eaa68-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="eaa68-119">-SqlVM</span></span>
<span data-ttu-id="eaa68-120">A configuração da máquina virtual SQL à qual a associação a um grupo será adicionada</span><span class="sxs-lookup"><span data-stu-id="eaa68-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="eaa68-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="eaa68-121">-SqlVMGroup</span></span>
<span data-ttu-id="eaa68-122">O grupo do sql virtual machine fará parte</span><span class="sxs-lookup"><span data-stu-id="eaa68-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="eaa68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa68-123">CommonParameters</span></span>
<span data-ttu-id="eaa68-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa68-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaa68-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa68-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="eaa68-126">INPUTS</span></span>

### <span data-ttu-id="eaa68-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="eaa68-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="eaa68-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="eaa68-128">OUTPUTS</span></span>

### <span data-ttu-id="eaa68-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="eaa68-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="eaa68-130">Notas</span><span class="sxs-lookup"><span data-stu-id="eaa68-130">NOTES</span></span>

## <span data-ttu-id="eaa68-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eaa68-131">RELATED LINKS</span></span>
