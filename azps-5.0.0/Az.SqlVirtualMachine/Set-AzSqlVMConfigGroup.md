---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115641"
---
# <span data-ttu-id="31787-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="31787-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="31787-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31787-102">SYNOPSIS</span></span>
<span data-ttu-id="31787-103">Defina as informações relativas a um grupo de máquinas virtuais SQL em uma configuração de máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="31787-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="31787-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31787-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31787-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31787-105">DESCRIPTION</span></span>
<span data-ttu-id="31787-106">O cmdlet Set-AzSqlVMConfigGroup define as informações necessárias para ingressar em um grupo de máquina virtual do SQL para uma configuração de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="31787-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="31787-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31787-107">EXAMPLES</span></span>

### <span data-ttu-id="31787-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31787-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="31787-109">Atualize a informations de grupo de uma configuração de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="31787-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="31787-110">OS</span><span class="sxs-lookup"><span data-stu-id="31787-110">PARAMETERS</span></span>

### <span data-ttu-id="31787-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="31787-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="31787-112">Senha da conta de inicialização do cluster</span><span class="sxs-lookup"><span data-stu-id="31787-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="31787-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="31787-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="31787-114">Senha da conta da operadora de cluster</span><span class="sxs-lookup"><span data-stu-id="31787-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="31787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31787-115">-DefaultProfile</span></span>
<span data-ttu-id="31787-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31787-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31787-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="31787-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="31787-118">Senha da conta de serviço do SQL</span><span class="sxs-lookup"><span data-stu-id="31787-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="31787-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="31787-119">-SqlVM</span></span>
<span data-ttu-id="31787-120">A configuração da máquina virtual do SQL à qual os membros do grupo serão adicionados</span><span class="sxs-lookup"><span data-stu-id="31787-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="31787-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="31787-121">-SqlVMGroup</span></span>
<span data-ttu-id="31787-122">O grupo do qual a máquina virtual do SQL fará parte</span><span class="sxs-lookup"><span data-stu-id="31787-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="31787-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31787-123">CommonParameters</span></span>
<span data-ttu-id="31787-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31787-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31787-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31787-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31787-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31787-126">INPUTS</span></span>

### <span data-ttu-id="31787-127">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="31787-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="31787-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31787-128">OUTPUTS</span></span>

### <span data-ttu-id="31787-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="31787-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="31787-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31787-130">NOTES</span></span>

## <span data-ttu-id="31787-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31787-131">RELATED LINKS</span></span>
