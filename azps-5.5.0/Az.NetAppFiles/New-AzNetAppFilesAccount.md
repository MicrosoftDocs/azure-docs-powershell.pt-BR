---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112932"
---
# <span data-ttu-id="681fd-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="681fd-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="681fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="681fd-102">SYNOPSIS</span></span>
<span data-ttu-id="681fd-103">Cria uma nova conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="681fd-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="681fd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="681fd-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="681fd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="681fd-105">DESCRIPTION</span></span>
<span data-ttu-id="681fd-106">O cmdlet **New-AzNetAppFilesAccount** cria uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="681fd-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="681fd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="681fd-107">EXAMPLES</span></span>

### <span data-ttu-id="681fd-108">Exemplo 1: Criar uma conta ANF</span><span class="sxs-lookup"><span data-stu-id="681fd-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="681fd-109">Esse comando cria a nova conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="681fd-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="681fd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="681fd-110">PARAMETERS</span></span>

### <span data-ttu-id="681fd-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="681fd-111">-ActiveDirectory</span></span>
<span data-ttu-id="681fd-112">Uma matriz de tabela hash que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="681fd-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681fd-113">-DefaultProfile</span></span>
<span data-ttu-id="681fd-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="681fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="681fd-115">-Local</span><span class="sxs-lookup"><span data-stu-id="681fd-115">-Location</span></span>
<span data-ttu-id="681fd-116">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="681fd-116">The location of the resource</span></span>

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

### <span data-ttu-id="681fd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="681fd-117">-Name</span></span>
<span data-ttu-id="681fd-118">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="681fd-118">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="681fd-120">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="681fd-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="681fd-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="681fd-121">-Tag</span></span>
<span data-ttu-id="681fd-122">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="681fd-122">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fd-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="681fd-123">-Confirm</span></span>
<span data-ttu-id="681fd-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="681fd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681fd-125">-WhatIf</span></span>
<span data-ttu-id="681fd-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="681fd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="681fd-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="681fd-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681fd-128">CommonParameters</span></span>
<span data-ttu-id="681fd-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681fd-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="681fd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681fd-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="681fd-131">INPUTS</span></span>

### <span data-ttu-id="681fd-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="681fd-132">None</span></span>

## <span data-ttu-id="681fd-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="681fd-133">OUTPUTS</span></span>

### <span data-ttu-id="681fd-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="681fd-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="681fd-135">Notas</span><span class="sxs-lookup"><span data-stu-id="681fd-135">NOTES</span></span>

## <span data-ttu-id="681fd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="681fd-136">RELATED LINKS</span></span>
