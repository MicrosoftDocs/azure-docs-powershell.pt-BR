---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127082"
---
# <span data-ttu-id="812a7-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="812a7-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="812a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="812a7-102">SYNOPSIS</span></span>
<span data-ttu-id="812a7-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="812a7-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="812a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="812a7-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="812a7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="812a7-105">DESCRIPTION</span></span>
<span data-ttu-id="812a7-106">O cmdlet **Remove-AzVMSqlServerExtension** remove uma extensão do AzureSQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="812a7-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="812a7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="812a7-107">EXAMPLES</span></span>

### <span data-ttu-id="812a7-108">Exemplo 1: Remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="812a7-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="812a7-109">Esse comando remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="812a7-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="812a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="812a7-110">PARAMETERS</span></span>

### <span data-ttu-id="812a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812a7-111">-DefaultProfile</span></span>
<span data-ttu-id="812a7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="812a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="812a7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="812a7-113">-Name</span></span>
<span data-ttu-id="812a7-114">Especifica o nome do SQL Server a extensão que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="812a7-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812a7-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="812a7-115">-NoWait</span></span>
<span data-ttu-id="812a7-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="812a7-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="812a7-117">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="812a7-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="812a7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812a7-118">-ResourceGroupName</span></span>
<span data-ttu-id="812a7-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="812a7-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812a7-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="812a7-120">-VMName</span></span>
<span data-ttu-id="812a7-121">Especifica o nome da máquina virtual da qual este cmdlet remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="812a7-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812a7-122">CommonParameters</span></span>
<span data-ttu-id="812a7-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812a7-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="812a7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812a7-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="812a7-125">INPUTS</span></span>

### <span data-ttu-id="812a7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="812a7-126">System.String</span></span>

## <span data-ttu-id="812a7-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="812a7-127">OUTPUTS</span></span>

### <span data-ttu-id="812a7-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="812a7-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="812a7-129">Notas</span><span class="sxs-lookup"><span data-stu-id="812a7-129">NOTES</span></span>

## <span data-ttu-id="812a7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="812a7-130">RELATED LINKS</span></span>

[<span data-ttu-id="812a7-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="812a7-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="812a7-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="812a7-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


